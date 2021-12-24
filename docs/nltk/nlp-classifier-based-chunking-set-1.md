# NLP |基于分类器的分块|集合 1

> 原文:[https://www . geesforgeks . org/NLP-基于分类器-组块-集合-1/](https://www.geeksforgeeks.org/nlp-classifier-based-chunking-set-1/)

`**ClassifierBasedTagger class**`从特征中学习，不像大多数词性标注者。`**ClassifierChunker class**`可以被创建为既能从单词又能从词性标签中学习，而不是像`**TagChunker class**`那样只从词性标签中学习。

使用来自`tree2conlltags()`的`chunk_trees2train_chunks()`，将(单词，位置，iob) 3 元组转换为((单词，位置，iob) 2 元组，以保持与训练 **`ClassiferBasedTagger class`** 所需的 2 元组(单词，位置)格式兼容。

**代码#1:我们来了解一下**

```py
# Loading Libraries
from nltk.chunk import ChunkParserI
from nltk.chunk.util import tree2conlltags, conlltags2tree
from nltk.tag import ClassifierBasedTagger

def chunk_trees2train_chunks(chunk_sents):

    # Using tree2conlltags
    tag_sents = [tree2conlltags(sent) for 
                 sent in chunk_sents]

    3-tuple is converted to 2-tuple
    return [[((w, t), c) for 
             (w, t, c) in sent] for sent in tag_sents]
```

现在，需要一个特征检测器函数来传递给分类器标签器。与 ClassifierChunker 类(下一步定义)一起使用的任何特征检测器函数都应该识别出标记是(单词，位置)元组的列表，并且具有与 prev_next_pos_iob()相同的函数签名。为了给分类器提供尽可能多的信息，这个特征集包含当前、前一个和下一个单词和词性标签，以及前一个 IOB 标签。

**代码#2:探测器功能**

```py
def prev_next_pos_iob(tokens, index, history):

    word, pos = tokens[index]
    if index == 0:
        prevword, prevpos, previob = ('<START>', )*3
    else:
        prevword, prevpos = tokens[index-1]
        previob = history[index-1]

    if index == len(tokens) - 1:
        nextword, nextpos = ('<END>', )*2
    else:
        nextword, nextpos = tokens[index + 1]
        feats = {'word': word,
                 'pos': pos,
                 'nextword': nextword,
                 'nextpos': nextpos,
                 'prevword': prevword,
                 'prevpos': prevpos,
                 'previob': previob
                 }
    return feats
```

现在，需要使用内部的`ClassifierBasedTagger` 和来自`chunk_trees2train_chunks()`的训练句子以及使用`prev_next_pos_iob()`提取的特征。作为`ChunkerParserI`的子类，`ClassifierChunker` 实现`parse()`方法，使用`conlltags2tree()`将内部标记器产生的((w，t)，c)元组转换为树

**代码#3 :**

```py
class ClassifierChunker(ChunkParserI):
    def __init__(self, train_sents, 
                 feature_detector = prev_next_pos_iob, **kwargs):

        if not feature_detector:
            feature_detector = self.feature_detector
            train_chunks = chunk_trees2train_chunks(train_sents)
            self.tagger = ClassifierBasedTagger(train = train_chunks,
            feature_detector = feature_detector, **kwargs)

    def parse(self, tagged_sent):

        if not tagged_sent: return None
        chunks = self.tagger.tag(tagged_sent)

        return conlltags2tree(
                [(w, t, c) for ((w, t), c) in chunks])
```
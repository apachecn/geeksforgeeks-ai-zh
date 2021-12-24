# NLP |基于训练标记器的组块器|集合 1

> 原文:[https://www . geesforgeks . org/NLP-training-tagger-based-chunker-set-1/](https://www.geeksforgeeks.org/nlp-training-tagger-based-chunker-set-1/)

训练组块器是手动指定正则表达式(正则表达式)组块模式的替代方法。但是手动训练来指定表达式是一项乏味的任务，因为它遵循命中和尝试的方法来获得准确的正确模式。因此，现有的语料库数据可以用来训练组块。

在下面的代码中，我们使用 **treebank_chunk 语料库**以树的形式生成分块句子。
- >要训练基于 tagger 的 chunker–**chunked _ sents()**方法由 TagChunker 类使用。
- >从树列表中提取 **(pos，iob)** 元组列表–TagChunker 类使用一个辅助函数， **conll_tag_chunks()** 。

然后这些元组最终被用来训练标记器。并且它学习用于词性标签的 IOB 标签。

**代码#1:让我们了解一下 Chunker 类的训练。**

```py
from nltk.chunk import ChunkParserI
from nltk.chunk.util import tree2conlltags, conlltags2tree
from nltk.tag import UnigramTagger, BigramTagger
from tag_util import backoff_tagger

def conll_tag_chunks(chunk_data):

    tagged_data = [tree2conlltags(tree) for 
                    tree in chunk_data]

    return [[(t, c) for (w, t, c) in sent] 
            for sent in tagged_data]

class TagChunker(ChunkParserI):

    def __init__(self, train_chunks, 
                 tagger_classes =[UnigramTagger, BigramTagger]):

        train_data = conll_tag_chunks(train_chunks)
        self.tagger = backoff_tagger(train_data, tagger_classes)

    def parse(self, tagged_sent):
        if not tagged_sent: 
            return None

        (words, tags) = zip(*tagged_sent)
        chunks = self.tagger.tag(tags)
        wtc = zip(words, chunks)

        return conlltags2tree([(w, t, c) for (w, (t, c)) in wtc])
```

**输出:**

```py
Training TagChunker

```

**代码#2:使用标签分块器。**

```py
# loading libraries
from chunkers import TagChunker
from nltk.corpus import treebank_chunk

# data from treebank_chunk corpus
train_data = treebank_chunk.chunked_sents()[:3000]
test_data = treebank_chunk.chunked_sents()[3000:]

# Initailazing 
chunker = TagChunker(train_data)
```

**代码#3:评估标签 Chunker**

```py
# testing
score = chunker.evaluate(test_data)

a = score.accuracy()
p = score.precision()
r = recall

print ("Accuracy of TagChunker : ", a)
print ("\nPrecision of TagChunker : ", p)
print ("\nRecall of TagChunker : ", r)
```

**输出:**

```py
Accuracy of TagChunker : 0.9732039335251428

Precision of TagChunker : 0.9166534370535006

Recall of TagChunker : 0.9465573770491803

```
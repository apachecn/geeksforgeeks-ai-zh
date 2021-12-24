# NLP |命名实体组块训练

> 原文:[https://www . geesforgeks . org/NLP-named-entity-chunker-training/](https://www.geeksforgeeks.org/nlp-named-entity-chunker-training/)

可以使用 **ieer 语料库**训练自命名实体组块器，该语料库代表**信息提取:实体识别**。 **ieer** 语料库有组块树，但是没有单词的词性标签，所以执行起来有点繁琐。

可以使用`ieertree2conlltags()`和`ieer_chunked_sents()`函数从 ieer 语料库创建命名实体块树。这可以用来训练在基于分类的组块中创建的`ClassifierChunker class`。

**代码# 1:ien ee 2 连体()**

```py
import nltk.tag
from nltk.chunk.util import conlltags2tree
from nltk.corpus import ieer

def ieertree2conlltags(tree, tag = nltk.tag.pos_tag):
    words, ents = zip(*tree.pos())
    iobs = []
    prev = None
    for ent in ents:
        if ent == tree.label():
            iobs.append('O')
            prev = None
        elif prev == ent:
            iobs.append('I-% s' % ent)
        else:
            iobs.append('B-% s' % ent)
            prev = ent

    words, tags = zip(*tag(words))

    return zip(words, tags, iobs)
```

**代码#2 : ieer_chunked_sents()**

```py
import nltk.tag
from nltk.chunk.util import conlltags2tree
from nltk.corpus import ieer

def ieer_chunked_sents(tag = nltk.tag.pos_tag):
    for doc in ieer.parsed_docs():
        tagged = ieertree2conlltags(doc.text, tag)
        yield conlltags2tree(tagged)
```

使用 94 个句子中的 80 个进行训练，其余的用于测试。

**代码#3:分类器如何在 treebank_chunk 语料库的第一句话上工作。**

```py
from nltk.corpus import ieer
from chunkers import ieer_chunked_sents, ClassifierChunker
from nltk.corpus import treebank_chunk

ieer_chunks = list(ieer_chunked_sents())

print ("Length of ieer_chunks : ", len(ieer_chunks))

# initializing chunker
chunker = ClassifierChunker(ieer_chunks[:80])
print("\nparsing : \n", chunker.parse(
        treebank_chunk.tagged_sents()[0]))

# evaluating
score = chunker.evaluate(ieer_chunks[80:])

a = score.accuracy()
p = score.precision()
r = score.recall()

print ("\nAccuracy : ", a)
print ("\nPrecision : ", p)
print ("\nRecall : ", r)
```

**输出:**

```py
Length of ieer_chunks : 94

parsing : 
Tree('S', [Tree('LOCATION', [('Pierre', 'NNP'), ('Vinken', 'NNP')]),
(', ', ', '), Tree('DURATION', [('61', 'CD'), ('years', 'NNS')]),
Tree('MEASURE', [('old', 'JJ')]), (', ', ', '), ('will', 'MD'), ('join', 'VB'), 
('the', 'DT'), ('board', 'NN'), ('as', 'IN'), ('a', 'DT'), ('nonexecutive', 'JJ'),
('director', 'NN'), Tree('DATE', [('Nov.', 'NNP'), ('29', 'CD')]), ('.', '.')])

Accuracy : 0.8829018388070625

Precision : 0.4088717454194793

Recall : 0.5053635280095352

```

**它是如何工作的？**
ieer _ chunked _ sents()生成的 ieer 树并不完全准确。没有明确的断句，所以每个文档都是一棵树。此外，这些单词没有被显式标记，它是使用 nltk.tag.pos_tag()进行猜测的。
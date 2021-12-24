# NLP |基于训练标记器的组块器|集合 2

> 原文:[https://www . geesforgeks . org/NLP-training-tagger-based-chunker-set-2/](https://www.geeksforgeeks.org/nlp-training-tagger-based-chunker-set-2/)

康乐 2000 团

使用 IOB 标签定义组块。

*   它指定块的开始和结束位置及其类型。
*   可以在这些 IOB 标记上训练词性标记器，以进一步为 ChunkerI 子类提供动力。
*   首先使用 **chunked_sents()** 方法 os 语料库，获得树，然后将其转换为可由词性标注器使用的格式。
*   **conll_tag_chunks()** 使用**tree 2 conltags()**将一个句子 Tree 转换为以下形式的三元组列表(word、pos、iob)。
    *   pos:词性标签
    *   iob : IOB 标签例如–B _ NP、I_NP 分别告诉工作在名词短语的开头和内部。
*   conlltags2tree()是 tree2conlltags()的反转
*   然后，三元组被转换成标记者可以识别的二元组。
*   RegexpParser 类对组块模式使用词性标记，因此词性标记的使用就像它们是要标记的单词一样。
*   **conll_tag_chunks()** 函数接受 3 元组(单词，pos，iob)并返回一个 2 元组列表，该列表的形式为(pos，iob)

**代码#1:我们来了解一下**

## 蟒蛇 3

```
from nltk.chunk.util import tree2conlltags, conlltags2tree
from nltk.tree import Tree

t = Tree('S', [Tree('NP', [('the', 'DT'), ('book', 'NN')])])

print ("Tree2conlltags : \n", tree2conlltags(t))

c = conlltags2tree([('the', 'DT', 'B-NP'), ('book', 'NN', 'I-NP')])

print ("\nconlltags2tree : \n", c)

# Converting 3 tuples to 2 tuples.
print ("\nconll_tag_chunnks for tree : \n", conll_tag_chunks([t]))
```

**输出:**

```
Tree2conlltags : 
[('the', 'DT', 'B-NP'), ('book', 'NN', 'I-NP')]

conlltags2tree : 
Tree('S', [Tree('NP', [('the', 'DT'), ('book', 'NN')])])

conll_tag_chunnks for tree : 
[[('DT', 'B-NP'), ('NN', 'I-NP')]]
```

**代码#2:使用 conll2000 语料库的 TagChunker 类**

## 蟒蛇 3

```
from chunkers import TagChunker
from nltk.corpus import conll2000

# data
conll_train = conll2000.chunked_sents('train.txt')
conll_test = conll2000.chunked_sents('test.txt')

# initializing the chunker
chunker = TagChunker(conll_train)

# testing
score = chunker.evaluate(conll_test)

a = score.accuracy()
p = score.precision()
r = recall

print ("Accuracy of TagChunker : ", a)
print ("\nPrecision of TagChunker : ", p)
print ("\nRecall of TagChunker : ", r)
```

**输出:**

```
Accuracy of TagChunker : 0.8950545623403762

Precision of TagChunker : 0.8114841974355675

Recall of TagChunker : 0.8644191676944863
```

**注:**conll2000 的性能不如 treebank_chunk，但 con ll 2000 是一个大得多的语料库。

**代码#3 : TagChunker 使用 UnigramTagger 类**

## 蟒蛇 3

```
# loading libraries
from chunkers import TagChunker
from nltk.tag import UnigramTagger

uni_chunker = TagChunker(train_chunks,
                         tagger_classes =[UnigramTagger])

score = uni_chunker.evaluate(test_chunks)

a = score.accuracy()

print ("Accuracy of TagChunker : ", a)
```

**输出:**

```
Accuracy of TagChunker : 0.9674925924335466
```

tagger_classes 参数直接传递给 backoff _ tagger()函数，因此这意味着它们必须是 SequentialBackoffTagger 的子类。在测试中，tagger_classes = [UnigramTagger，BigramTagger]的默认值通常会产生最佳结果，但它会因不同的语料库而异。
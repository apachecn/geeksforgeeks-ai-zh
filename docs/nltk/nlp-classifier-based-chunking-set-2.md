# NLP |基于分类器的分块|集合 2

> 原文:[https://www . geesforgeks . org/NLP-基于分类器-组块-集合-2/](https://www.geeksforgeeks.org/nlp-classifier-based-chunking-set-2/)

使用 treebank_chunk 语料库中的数据，让我们评估组块(在上一篇文章中准备好的)。

**代码#1 :**

```py
# loading libraries
from chunkers import ClassifierChunker
from nltk.corpus import treebank_chunk

train_data = treebank_chunk.chunked_sents()[:3000]
test_data = treebank_chunk.chunked_sents()[3000:]

# initializing
chunker = ClassifierChunker(train_data)

# evaluation
score = chunker.evaluate(test_data)

a = score.accuracy()
p = score.precision()
r = recall

print ("Accuracy of ClassifierChunker : ", a)
print ("\nPrecision of ClassifierChunker : ", p)
print ("\nRecall of ClassifierChunker : ", r)
```

**输出:**

```py
Accuracy of ClassifierChunker : 0.9721733155838022

Precision of ClassifierChunker : 0.9258838793383068

Recall of ClassifierChunker : 0.9359016393442623

```

**代码#2:我们来对比一下 conll_train** 的表现

```py
chunker = ClassifierChunker(conll_train)
score = chunker.evaluate(conll_test)

a = score.accuracy()
p = score.precision()
r = score.recall()

print ("Accuracy of ClassifierChunker : ", a)
print ("\nPrecision of ClassifierChunker : ", p)
print ("\nRecall of ClassifierChunker : ", r)
```

**输出:**

```py
Accuracy of ClassifierChunker : 0.9264622074002153

Precision of ClassifierChunker : 0.8737924310910219

Recall of ClassifierChunker : 0.9007354620620346

```

单词可以通过 tagger 传递到我们的特征检测器函数中，通过创建嵌套的 2-元组的形式((word，pos)，iob)，chunk_trees2train_chunks()方法产生这些嵌套的 2-元组。
提取以下特征:

*   当前单词和词性标记
*   前一个单词和 IOB 标记，词性标记
*   下一个单词和词性标签

ClassifierChunker 类使用一个内部的 ClassifierBasedTagger 和 prev_next_pos_iob()作为它的默认功能检测器。标记器的结果采用相同的嵌套 2 元组形式，然后使用 conlltags2tree()将其重新格式化为 3 元组，以返回最终的 Tree。

**代码#3:不同的分类器构建器**

```py
# loading libraries
from chunkers import ClassifierChunker
from nltk.corpus import treebank_chunk
from nltk.classify import MaxentClassifier

train_data = treebank_chunk.chunked_sents()[:3000]
test_data = treebank_chunk.chunked_sents()[3000:]

builder = lambda toks: MaxentClassifier.train(
            toks, trace = 0, max_iter = 10, min_lldelta = 0.01)

chunker = ClassifierChunker(
        train_data, classifier_builder = builder)

score = chunker.evaluate(test_data)

a = score.accuracy()
p = score.precision()
r = score.recall()

print ("Accuracy of ClassifierChunker : ", a)
print ("\nPrecision of ClassifierChunker : ", p)
print ("\nRecall of ClassifierChunker : ", r)
```

**输出:**

```py
Accuracy of ClassifierChunker : 0.9743204362949285

Precision of ClassifierChunker : 0.9334423548650859

Recall of ClassifierChunker : 0.9357377049180328

```

ClassifierBasedTagger 类默认使用 NaiveBayesClassifier.train 作为其分类器 _builder。但是任何分类器都可以通过重写 classifier_builder 关键字参数来使用。
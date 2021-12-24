# NLP |三元组标签(TnT)标记

> 原文:[https://www . geesforgeks . org/NLP-trigramsntags-TNT-taging/](https://www.geeksforgeeks.org/nlp-trigramsntags-tnt-tagging/)

**TnT Tagger :** 它是一个在二阶马尔可夫模型上工作的统计 Tagger。

*   它是一个非常高效的词性标注器，可以在不同的语言和任何标注集上进行训练。
*   对于参数生成，组件在标记的语料库上训练。它结合了不同的平滑和处理未知单词的方法
*   线性插值用于平滑，相应的权重由删除的插值确定。

TnT 标记器与普通标记器有不同的 API。可以在创建 train()方法后显式使用它。

**代码#1:使用列车()方法**

```py
from nltk.tag import tnt
from nltk.corpus import treebank

# initializing training and testing set    
train_data = treebank.tagged_sents()[:3000]
test_data = treebank.tagged_sents()[3000:]

# initializing tagger
tnt_tagging = tnt.TnT()

# training
tnt_tagging.train(train_data)

# evaluating
a = tnt_tagging.evaluate(test_data)

print ("Accuracy of TnT Tagging : ", a)
```

**输出:**

```py
Accuracy of TnT Tagging : 0.8756313403842003

```

**了解 TnT tagger 的工作情况:**

*   它保持了
    *   内部频率分布
    *   ConditionalFreqDist，它基于训练数据。
*   频率分布(FreqDist)计算单项式、二元式和三元式。
*   这些频率用于计算每个单词的可能标签的概率。
*   TnT tagger 将所有 ngram 模型一起使用来选择最佳标签，而不是构建 NgramTagger 子类的退避链。
*   基于每个可能标签的概率，它为整个句子选择最可能的模型。

**代码#2:对未知单词使用 tagger 作为‘unk’**

```py
from nltk.tag import tnt
from nltk.corpus import treebank
from nltk.tag import DefaultTagger

# initializing training and testing set    
train_data = treebank.tagged_sents()[:3000]
test_data = treebank.tagged_sents()[3000:]

# initializing tagger
unk = DefaultTagger('NN')
tnt_tagging = tnt.TnT(unk = unk, Trained = True)

# training 
tnt_tagging.train(train_data)

# evaluating
a = tnt_tagging.evaluate(test_data)

print ("Accuracy of TnT Tagging : ", a)
```

**输出:**

```py
Accuracy of TnT Tagging : 0.892467083962875

```

*   unknown tagger 的 tag()方法仅用单个单词句子调用。
*   TnT tagger 可以将未知单词的 tagger 作为 unk 传入。
*   如果这个标记已经被训练过了，你可以通过训练=真。
*   否则，它将调用 unk.train(数据)，其数据与传递给 train()方法的数据相同。

**控制波束搜索:**

*   要为 TnT 修改的另一个参数是 **N** ，即它控制标记器维护的可能解决方案的数量。
*   默认情况下，N = 1000。
*   如果增加 N 的值，内存量会增加，但精度不会有任何具体的增加。
*   如果减少 N 的值，内存量会减少，但会降低精度。

**代码#3:使用 N = 100**

```py
from nltk.tag import tnt
from nltk.corpus import treebank
from nltk.tag import DefaultTagger

# initializing training and testing set    
train_data = treebank.tagged_sents()[:3000]
test_data = treebank.tagged_sents()[3000:]

# initializing tagger
tnt_tagger = tnt.TnT(N = 100)

# training 
tnt_tagging.train(train_data)

# evaluating
a = tnt_tagging.evaluate(test_data)

print ("Accuracy of TnT Tagging : ", a)
```

**输出:**

```py
Accuracy of TnT Tagging : 0.8756313403842003

```
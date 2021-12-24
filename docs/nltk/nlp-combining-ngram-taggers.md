# NLP |组合 NGram 标记器

> 原文:[https://www.geeksforgeeks.org/nlp-combining-ngram-taggers/](https://www.geeksforgeeks.org/nlp-combining-ngram-taggers/)

NgramTagger 有 3 个子类

*   UnigramTagger
*   bigrammatagger
*   trigrammatagger

BigramTagger 子类使用前一个标签作为其上下文的一部分
trigrammatagger 子类使用前两个标签作为其上下文的一部分。

**ngram**–它是 n 个项目的子序列。
**NgramTagger 子类的想法:**

*   通过查看前面的单词和 P-O-S 标签，可以猜到当前单词的词性标签。
*   每个标记器维护一个上下文字典(ContextTagger 父类用于实现它)。
*   本词典用于根据上下文猜测标签。
*   在 NgramTagger 子类的情况下，上下文是一些先前标记的单词。

**代码# 1:Bigram tagger 的工作**

```
# Loading Libraries 
from nltk.tag import DefaultTagger 
from nltk.tag import BigramTagger

from nltk.corpus import treebank

# initializing training and testing set    
train_data = treebank.tagged_sents()[:3000]
test_data = treebank.tagged_sents()[3000:]

# Tagging
tag1 = BigramTagger(train_data)

# Evaluation
tag1.evaluate(test_data)
```

**输出:**

```
0.11318799913662854

```

**代码#2:三元标记器**的工作

```
# Loading Libraries 
from nltk.tag import DefaultTagger 
from nltk.tag import TrigramTagger

from nltk.corpus import treebank

# initializing training and testing set    
train_data = treebank.tagged_sents()[:3000]
test_data = treebank.tagged_sents()[3000:]

# Tagging
tag1 = TrigramTagger(train_data)

# Evaluation
tag1.evaluate(test_data)
```

**输出:**

```
0.06876753723289446

```

**代码#3:集体使用 Unigram、Bigram 和 Trigram tagger。**

```
# Loading Libraries

from nltk.tag import TrigramTagger
from tag_util import backoff_tagger
from nltk.corpus import treebank

# initializing training and testing set    
train_data = treebank.tagged_sents()[:3000]
test_data = treebank.tagged_sents()[3000:]

backoff = DefaultTagger('NN')
tag = backoff_tagger(train_sents, 
                     [UnigramTagger, BigramTagger, TrigramTagger], 
                     backoff = backoff)

tag.evaluate(test_sents)
```

**输出:**

```
0.8806820634578028

```

**它是如何工作的？**

*   **back _ tagger**函数创建每个 tagger 类的一个实例。
*   它将以前的标记和训练作为一种补偿。
*   Tagger 类的顺序很重要:在上面的代码中，第一个类是 UnigramTagger，因此，它将首先被训练，并被赋予初始退避 tagger(默认 tagger)。
*   然后，这个标记器成为下一个标记器类的回退标记器。
*   返回的最终标记器将是最后一个标记器类的实例–**触发标记器**。

**代码#4:证明**

```
print (tagger._taggers[-1] == backoff)

print ("\n", isinstance(tagger._taggers[0], TrigramTagger))

print ("\n", isinstance(tagger._taggers[1], BigramTagger))
```

**输出:**

```
True

True

True

```
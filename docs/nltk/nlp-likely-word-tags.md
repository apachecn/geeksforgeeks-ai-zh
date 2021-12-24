# NLP |可能的单词标签

> 原文:[https://www.geeksforgeeks.org/nlp-likely-word-tags/](https://www.geeksforgeeks.org/nlp-likely-word-tags/)

**nltk . probability . freqdist**用于通过统计树库语料库中的词频来查找最常见的单词。**conditionalreqdist**类是为带标签的单词创建的，我们计算每个单词每个标签的出现频率。然后这些计数被用来构建一个频繁单词的模型作为关键字，每个单词的最频繁标签作为一个值。

**代码#1:创建功能**

```
# Loading Libraries
from nltk.probability import FreqDist, ConditionalFreqDist

# Making function
def word_tag_model(words, tagged_words, limit = 200):

    fd = FreqDist(words)
    cfd = ConditionalFreqDist(tagged_words)
    most_freq = (word for word, count in fd.most_common(limit))

return dict((word, cfd[word].max()) 
             for word in most_freq)
```

**代码#2:使用带有 UnigramTagger 的函数**

```
# loading libraries
from tag_util import word_tag_model
from nltk.corpus import treebank
from nltk.tag import UnigramTagger

# initializing training and testing set    
train_data = treebank.tagged_sents()[:3000]
test_data = treebank.tagged_sents()[3000:]

# Initializing the model
model = word_tag_model(treebank.words(), 
                       treebank.tagged_words())

# Initializing the Unigram
tag = UnigramTagger(model = model)

print ("Accuracy : ", tag.evaluate(test_data))
```

**输出:**

```
Accuracy : 0.559680552557738

```

**代码#3:让我们试试回退链**

```
# Loading libraries
from nltk.tag import UnigramTagger
from nltk.tag import DefaultTagger

default_tagger = DefaultTagger('NN')

likely_tagger = UnigramTagger(
        model = model, backoff = default_tagger)

tag = backoff_tagger(train_sents, [
        UnigramTagger, BigramTagger, 
        TrigramTagger], backoff = likely_tagger)

print ("Accuracy : ", tag.evaluate(test_data))
```

**输出:**

```
Accuracy : 0.8806820634578028

```

**注意:**退避链有增加精度。我们可以通过有效地使用 UnigramTagger 类来进一步改进这个结果。

**代码#4:手动覆盖训练有素的标记员**

```
# Loading libraries
from nltk.tag import UnigramTagger
from nltk.tag import DefaultTagger

default_tagger = DefaultTagger('NN')

tagger = backoff_tagger(train_sents, [
        UnigramTagger, BigramTagger,
        TrigramTagger], backoff = default_tagger)

likely_tag = UnigramTagger(model = model, backoff = tagger)

print ("Accuracy : ", likely_tag.evaluate(test_data))
```

**输出:**

```
Accuracy : 0.8824088063889488

```
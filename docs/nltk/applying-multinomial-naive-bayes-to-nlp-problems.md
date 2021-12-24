# 将多项式朴素贝叶斯应用于自然语言处理问题

> 原文:[https://www . geesforgeks . org/application-多项式-朴素贝叶斯-nlp-problems/](https://www.geeksforgeeks.org/applying-multinomial-naive-bayes-to-nlp-problems/)

[朴素贝叶斯分类器](https://www.geeksforgeeks.org/naive-bayes-classifiers/)算法是一族基于应用贝叶斯定理的概率算法，假设每对特征之间条件独立。
贝叶斯定理计算概率 P(c|x)，其中 c 是可能结果的类别，x 是必须分类的给定实例，代表某些特定特征。
**P(c | x)= P(x | c)* P(c)/P(x)**
朴素贝叶斯多用于自然语言处理(NLP)问题。朴素贝叶斯预测文本的标签。他们计算给定文本的每个标签的概率，然后输出最高的标签。
**朴素贝叶斯算法是如何工作的？**
我们来举个例子，把复习分门别类不管是正面还是负面。
训练数据集:

<figure class="table">

| 文本 | 复习 |
| --- | --- |
| “我喜欢这部电影” | 积极的 |
| “这是一部好电影。好故事” | 积极的 |
| “好歌。但可悲的无聊结局。” | 否定的；消极的；负面的；负的 |
| “男主角演技不好但女主角长得好看。总的来说是部好电影 | 积极的 |
| 《悲伤无聊的电影》 | 否定的；消极的；负面的；负的 |

</figure>

我们对文本“总体上喜欢这部电影”是正面评价还是负面评价进行分类。我们要计算，
**P(正|整体喜欢这部电影)**——给定句子是“整体喜欢这部电影”的情况下，句子的标签为正的概率。
**P(否定|整体喜欢这部电影)**——假设句子是“整体喜欢这部电影”，那么句子的标签为否定的概率。
在此之前，首先，我们在文本中应用移除停用词和词干。
**移除 Stopwords** :这些都是常见的词，并不会真正给分类增加什么，比如一个 able、要么、else、ever 等等。
**词干**:词干取出词根。
现在应用这两种技术后，我们的文本变成了

<figure class="table">

| 文本 | 复习 |
| --- | --- |
| " ilikedthemovi " | 积极的 |
| " itsagoodmovienicestori " | 积极的 |
| "美好的歌但是悲伤的歌" | 否定的；消极的；负面的；负的 |
| " heroscatingisbadbutheronelooksgoodoveralnicemovi " | 积极的 |
| 《sadboringmovi》 | 否定的；消极的；负面的；负的 |

</figure>

**特征工程:**
重要的部分是从数据中找到特征，让机器学习算法发挥作用。在这种情况下，我们有文本。我们需要将这些文本转换成数字，以便进行计算。我们使用词频。也就是把每一份文件都看作是它包含的一组单词。我们的特点将是这些词的计数。
在我们的例子中，我们有 *P(正面|整体喜欢电影)*，通过使用这个定理:

> **P(正面|整体喜欢电影)** = P(整体喜欢电影|正面)* P(正面)/ P(整体喜欢电影)

因为对于我们的分类器，我们必须找出哪个标签具有更大的概率，所以我们可以丢弃对于两个标签都相同的除数，
P(总体喜欢电影|正)* P(正)与 P(总体喜欢电影|负)* P(负)
但是有一个问题:“总体喜欢电影”没有出现在我们的训练数据集中，所以概率为零。这里，我们假设**“幼稚”**条件，即一个句子中的每个单词都独立于其他单词。这意味着现在我们看单个单词。
我们可以这样写:

> P(整体喜欢这部电影)= P(整体)* P(喜欢)* P(the) * P(电影)

下一步就是应用贝叶斯定理:-

> **P(整体喜欢电影|正面)** = P(整体|正面)* P(喜欢|正面)* P(the |正面)* P(电影|正面)

而现在，这些个别的词实际上在我们的训练数据中出现了好几次，我们可以计算出来！
**计算概率:**
首先，我们计算每个标签的先验概率:对于我们训练数据中的给定句子，其为正 P(正)的概率为 3/5。那么，P(负)是 2/5。
那么，计算 P(整体|正)就是计算“整体”这个词在正片(1)中出现的次数除以正片(11)中的总字数。因此，P(整体|正)= 1/17，P(喜欢/正)= 1/17，P(该/正)= 2/17，P(电影/正)= 3/17。
如果概率为零，那么通过使用拉普拉斯平滑:我们将每个计数加 1，所以它永远不会为零。为了平衡这一点，我们把可能的字数加到除数上，所以除法永远不会大于 1。在我们的例子中，总的可能字数是 21。
应用平滑，结果为:

<figure class="table">

| 单词 | p(字&#124;正) | p(单词&#124;否定) |
| --- | --- | --- |
| 全部的 | 1 + 1/17 + 21 | 0 + 1/7 + 21 |
| 喜欢 | 1 + 1/17 + 21 | 0 + 1/7 + 21 |
| 这 | 2 + 1/17 + 21 | 0 + 1/7 + 21 |
| 电影 | 3 + 1/17 + 21 | 1 + 1/7 + 21 |

</figure>

现在我们把所有的概率相乘，看看谁更大:

> p(整体|正)* P(喜欢|正)* P(the |正)* P(电影|正)* P(正)= 1.38 * 10^{-5} = 0.0000138
> P(整体|负)* P(喜欢|负)* P(the |负)* P(电影|负)* P(负)= 0.13 * 10^{-5} = 0.0000013

我们的分类器给出了“总体喜欢这部电影”的肯定标签。
下面是实现:

## 蟒蛇 3

```
# cleaning texts
import pandas as pd
import re
import nltk
from nltk.corpus import stopwords
from nltk.stem.porter import PorterStemmer
from sklearn.feature_extraction.text import CountVectorizer

dataset = [["I liked the movie", "positive"],
           ["It’s a good movie. Nice story", "positive"],
           ["Hero’s acting is bad but heroine looks good.\
            Overall nice movie", "positive"],
            ["Nice songs. But sadly boring ending.", "negative"],
            ["sad movie, boring movie", "negative"]]

dataset = pd.DataFrame(dataset)
dataset.columns = ["Text", "Reviews"]

nltk.download('stopwords')

corpus = []

for i in range(0, 5):
    text = re.sub('[^a-zA-Z]', '', dataset['Text'][i])
    text = text.lower()
    text = text.split()
    ps = PorterStemmer()
    text = ''.join(text)
    corpus.append(text)

# creating bag of words model
cv = CountVectorizer(max_features = 1500)

X = cv.fit_transform(corpus).toarray()
y = dataset.iloc[:, 1].values
```

## 蟒蛇 3

```
# splitting the data set into training set and test set
from sklearn.cross_validation import train_test_split

X_train, X_test, y_train, y_test = train_test_split(
           X, y, test_size = 0.25, random_state = 0)
```

## 蟒蛇 3

```
# fitting naive bayes to the training set
from sklearn.naive_bayes import GaussianNB
from sklearn.metrics import confusion_matrix

classifier = GaussianNB();
classifier.fit(X_train, y_train)

# predicting test set results
y_pred = classifier.predict(X_test)

# making the confusion matrix
cm = confusion_matrix(y_test, y_pred)
cm
```
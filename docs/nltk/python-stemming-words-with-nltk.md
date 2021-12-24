# Python |用 NLTK 词干

> 原文:[https://www . geesforgeks . org/python-词干-words-with-nltk/](https://www.geeksforgeeks.org/python-stemming-words-with-nltk/)

先决条件:[词干入门](https://www.geeksforgeeks.org/introduction-to-stemming/)
词干是产生词根/基本词的形态变体的过程。词干程序通常被称为词干算法或词干分析器。词干算法将单词“巧克力”、“巧克力”、“巧克力”简化为词根单词，“巧克力”和“检索”、“检索”、“检索”简化为词干“检索”。

```
Some more example of stemming for root word "like" include:

-> "likes"
-> "liked"
-> "likely"
-> "liking"
```

**词干错误:**
词干错误主要有两个–***超越*** 和 ***不足*** 。当两个词干相同但词干不同时，就会出现词干过度。词干不足发生在两个词词干相同但词干不同的时候。

**炮泥的应用有:**

*   词干用于信息检索系统，如搜索引擎。
*   它用于确定领域分析中的领域词汇。

词干是可取的，因为它可以减少冗余，因为大多数情况下词干和它们的屈折/派生单词意思相同。

下面是使用 NLTK 词干的实现:

**代码#1:**

## 蟒蛇 3

```
# import these modules
from nltk.stem import PorterStemmer
from nltk.tokenize import word_tokenize

ps = PorterStemmer()

# choose some words to be stemmed
words = ["program", "programs", "programmer", "programming", "programmers"]

for w in words:
    print(w, " : ", ps.stem(w))
```

**输出:**

```
program  :  program
programs  :  program
programmer  :  program
programming  :  program
programmers  :  program
```

**代码#2:** 从句子中提取单词

## 蟒蛇 3

```
# importing modules
from nltk.stem import PorterStemmer
from nltk.tokenize import word_tokenize

ps = PorterStemmer()

sentence = "Programmers program with programming languages"
words = word_tokenize(sentence)

for w in words:
    print(w, " : ", ps.stem(w))
```

**输出:**

```
Programmers  :  program
program  :  program
with  :  with
programming  :  program
languages  :  languag
```
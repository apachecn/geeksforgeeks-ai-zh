# NLP | Regex 和词缀标注

> 原文:[https://www.geeksforgeeks.org/nlp-regex-and-affix-tagging/](https://www.geeksforgeeks.org/nlp-regex-and-affix-tagging/)

正则表达式匹配用于标记单词。考虑这个例子，数字可以与\d 匹配来分配标签 CD(指基数)。或者可以匹配已知的单词模式，例如后缀“ing”。

**理解概念–**

*   RegexpTagger 是 SequentialBackoffTagger 的一个子类。它可以位于 DefaultTagger 类之前，以便标记 n-gram 标记器遗漏的单词，因此可以成为退避链的有用部分。
*   在初始化时，模式被保存在 RegexpTagger 类中。然后调用 choose_tag()，它迭代模式。然后，它使用 re.match()返回能够匹配当前单词的第一个表达式标记。
*   因此，如果两个给定的表达式匹配，那么第一个表达式的标记将被返回，甚至不用尝试第二个表达式。
*   如果给定的模式像–( r’。*、' NN ')、RegexpTagger 类可以替换 DefaultTagger 类

**代码#1 : Python 正则表达式模块和 re 语法**

## 蟒蛇 3

```py
patterns = [(r'^\d+{content}apos;, 'CD'),
            # gerunds, i.e. wondering
            (r'.*ing{content}apos;, 'VBG'),
            # i.e. wonderment
            (r'.*ment{content}apos;, 'NN'),
            # i.e. wonderful
            (r'.*ful{content}apos;, 'JJ')]
```

**RegexpTagger** 类需要一个二元组列表

```py
-> first element in the tuple is a regular expression
-> second element is the tag
```

**代码#2:使用正则表达式**

## 蟒蛇 3

```py
# Loading Libraries
from tag_util import patterns
from nltk.tag import RegexpTagger
from nltk.corpus import treebank

test_data = treebank.tagged_sents()[3000:]

tagger = RegexpTagger(patterns)
print ("Accuracy : ", tagger.evaluate(test_data))
```

**输出:**

```py
Accuracy : 0.037470321605870924
```

**什么是词缀标注？**
是 ContextTagger 的子类。在词缀标记类的情况下，上下文要么是单词的后缀，要么是单词的前缀。因此，它清楚地表明，这个类可以基于单词开头或结尾的固定长度子字符串来学习标签。
指定三个字符的后缀。单词长度必须至少为 5 个字符，如果单词少于 5 个字符，则返回无作为标记。

**代码#3:理解词缀标记。**

## 蟒蛇 3

```py
# loading libraries
from tag_util import word_tag_model
from nltk.corpus import treebank
from nltk.tag import AffixTagger

# initializing training and testing set   
train_data = treebank.tagged_sents()[:3000]
test_data = treebank.tagged_sents()[3000:]

print ("Train data : \n", train_data[1])

# Initializing tagger
tag = AffixTagger(train_data)

# Testing
print ("\nAccuracy : ", tag.evaluate(test_data))
```
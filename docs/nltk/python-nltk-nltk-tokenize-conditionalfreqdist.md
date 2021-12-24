# Python | NLTK NLTK . token ize . conditionalreqdist()

> 原文:[https://www . geeksforgeeks . org/python-nltk-nltk-token ize-conditionalforgedist/](https://www.geeksforgeeks.org/python-nltk-nltk-tokenize-conditionalfreqdist/)

借助`**nltk.tokenize.ConditionalFreqDist()**`方法，我们可以用`tokenize.ConditionalFreqDist()`方法统计一个句子中单词的出现频率。

> **语法:** `tokenize.ConditionalFreqDist()`
> **返回:** **返回字典中单词的频率分布。**

**例#1 :**
在这个例子中我们可以看到，通过使用`tokenize.ConditionalFreqDist()`方法，我们能够统计一个句子中单词的出现次数。

```
# import ConditionalFreqDist() method from nltk
from nltk.probability import ConditionalFreqDist
from nltk.tokenize import word_tokenize

# Create a reference variable for Class SExprTokenizer
tk = ConditionalFreqDist()

# Create a string input
gfg = "Geeks for Geeks"

for word in word_tokenize(gfg):
   condition = len(word)
   tk[condition][word] += 1

print(tk)
```

**输出:**

> FreqDist({“极客”:2，“for”:1 })

**例 2 :**

```
# import ConditionalFreqDist() method from nltk
from nltk.probability import ConditionalFreqDist
from nltk.tokenize import word_tokenize

# Create a reference variable for Class SExprTokenizer
tk = ConditionalFreqDist()

# Create a string input
gfg = "G F G"

for word in word_tokenize(gfg):
   condition = len(word)
   tk[condition][word] += 1

print(tk)
```

**输出:**

> freqdis({ ' g ':' 2，' f ':' 1 })
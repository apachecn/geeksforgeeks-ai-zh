# Python NLTK | NLTK . token izer . word _ token ize()

> 原文:[https://www . geesforgeks . org/python-nltk-nltk-token izer-word _ token ize/](https://www.geeksforgeeks.org/python-nltk-nltk-tokenizer-word_tokenize/)

借助`**nltk.tokenize.word_tokenize()**`方法，我们能够使用`tokenize.word_tokenize()`方法从字符串中提取标记。它实际上从一个单词中返回**音节**。一个单词可以包含一两个音节。

> **语法:** `tokenize.word_tokenize()`
> **返回:** **返回单词的音节列表。**

**示例#1 :**
在这个示例中，我们可以看到，通过使用`tokenize.word_tokenize()`方法，我们能够从单词或句子流中提取音节。

```
# import SyllableTokenizer() method from nltk
from nltk import word_tokenize

# Create a reference variable for Class word_tokenize
tk = SyllableTokenizer()

# Create a string input
gfg = "Antidisestablishmentarianism"

# Use tokenize method
geek = tk.tokenize(gfg)

print(geek)
```

**输出:**

> ['An '，' ti '，' dis '，' es '，' ta '，' blish '，' men '，' ta '，' ria '，' ism']

**例 2 :**

```
# import SyllableTokenizer() method from nltk
from nltk.tokenize import word_tokenize

# Create a reference variable for Class word_tokenize
tk = SyllableTokenizer()

# Create a string input
gfg = "Gametophyte"

# Use tokenize method
geek = tk.tokenize(gfg)

print(geek)
```

**输出:**

> ['Ga '，' me '，' to '，' phy '，' te']
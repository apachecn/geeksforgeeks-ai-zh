# python nltk | nltk . token ize . mwe()

> 原文:[https://www . geesforgeks . org/python-nltk-nltk-token ize-mwe/](https://www.geeksforgeeks.org/python-nltk-nltk-tokenize-mwe/)

借助`**NLTK nltk.tokenize.mwe()**`方法，我们可以将音频流标记为多词表达标记，这有助于使用`nltk.tokenize.mwe()`方法将标记与下划线绑定。请记住它区分大小写。

> **语法:** `MWETokenizer.tokenize()`
> **返回:** **返回绑定令牌，就像之前声明的一样。**

**示例#1 :**
在此示例中，我们使用了`MWETokenizer.tokenize()`方法，该方法用于绑定之前定义的令牌。我们也可以使用`tokenizer.add_mwe()`方法添加预定义的令牌。

```
# import MWETokenizer() method from nltk
from nltk.tokenize import MWETokenizer

# Create a reference variable for Class MWETokenizer
tk = MWETokenizer([('g', 'f', 'g'), ('geeks', 'for', 'geeks')])

# Create a string input
gfg = "geeks for geeks g f g"

# Use tokenize method
geek = tk.tokenize(gfg.split())

print(geek)
```

**输出:**

> ['geeks_for_geeks '，' g_f_g']

**例 2 :**

```
# import MWETokenizer() method from nltk
from nltk.tokenize import MWETokenizer

# Create a reference variable for Class MWETokenizer
tk = MWETokenizer([('g', 'f', 'g'), ('geeks', 'for', 'geeks')])
tk.add_mwe(('who', 'are', 'you'))

# Create a string input
gfg = "who are you at geeks for geeks"

# Use tokenize method
geek = tk.tokenize(gfg.split())

print(geek)
```

**输出:**

> ['你是谁'，' at '，'极客的极客'
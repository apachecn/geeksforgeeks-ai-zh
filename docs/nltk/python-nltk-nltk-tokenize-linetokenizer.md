# python nltk | nltk . token ize . lineokenizer

> 原文:[https://www . geesforgeks . org/python-nltk-nltk-token ize-line token izer/](https://www.geeksforgeeks.org/python-nltk-nltk-tokenize-linetokenizer/)

借助`**nltk.tokenize.LineTokenizer()**`方法，我们能够使用`tokenize.LineTokenizer()`方法从单行形式的句子串中提取标记。

> **语法:** `tokenize.LineTokenizer()`
> **返回:**从句子流中返回行的标记。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`tokenize.LineTokenizer()`方法，我们能够将句子流中的标记提取为小行。

```py
# import LineTokenizer() method from nltk
from nltk.tokenize import LineTokenizer

# Create a reference variable for Class LineTokenizer
tk = LineTokenizer()

# Create a string input
gfg = "GeeksforGeeks...$&* \nis\n for geeks"

# Use tokenize method
geek = tk.tokenize(gfg)

print(geek)
```

**输出:**

> [“极客”…$ & *‘是’，‘代表极客’]

**例 2 :**

```py
# import LineTokenizer() method from nltk
from nltk.tokenize import LineTokenizer

# Create a reference variable for Class LineTokenizer
tk = LineTokenizer(blanklines ='keep')

# Create a string input
gfg = "The price\n\n of burger \nin BurgerKing is Rs.36.\n"

# Use tokenize method
geek = tk.tokenize(gfg)

print(geek)
```

**输出:**

> [“汉堡的价格”是 36 卢比]
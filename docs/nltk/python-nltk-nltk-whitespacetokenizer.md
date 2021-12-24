# python nltk | nltk . white space token izer

> 原文:[https://www . geesforgeks . org/python-nltk-nltk-white spacetokenizer/](https://www.geeksforgeeks.org/python-nltk-nltk-whitespacetokenizer/)

借助`**nltk.tokenize.WhitespaceTokenizer()**`方法，我们可以使用`tokenize.WhitespaceTokenizer()`方法从没有**空格**、**新行**和**标签**的单词或句子串中提取标记。

> **语法:** `tokenize.WhitespaceTokenizer()`
> **返回:** **从字符串中返回令牌**

**示例#1 :**
在这个示例中，我们可以看到，通过使用`tokenize.WhitespaceTokenizer()`方法，我们能够从单词流中提取标记。

```py
# import WhitespaceTokenizer() method from nltk
from nltk.tokenize import WhitespaceTokenizer

# Create a reference variable for Class WhitespaceTokenizer
tk = WhitespaceTokenizer()

# Create a string input
gfg = "GeeksforGeeks \nis\t for geeks"

# Use tokenize method
geek = tk.tokenize(gfg)

print(geek)
```

**输出:**

> ['GeeksforGeeks '，' is '，' for '，' geeks']

**例 2 :**

```py
# import WhitespaceTokenizer() method from nltk
from nltk.tokenize import WhitespaceTokenizer

# Create a reference variable for Class WhitespaceTokenizer
tk = WhitespaceTokenizer()

# Create a string input
gfg = "The price\t of burger \nin BurgerKing is Rs.36.\n"

# Use tokenize method
geek = tk.tokenize(gfg)

print(geek)
```

**输出:**

> ['The '，' price '，' of '，' burger '，' in '，' BurgerKing '，' is '，' Rs.36.']
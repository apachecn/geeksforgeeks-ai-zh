# python nltk | nltk . token ize . tabtoken izer()

> 原文:[https://www . geesforgeks . org/python-nltk-nltk-token ize-tabtokingizer/](https://www.geeksforgeeks.org/python-nltk-nltk-tokenize-tabtokenizer/)

借助`**nltk.tokenize.TabTokenizer()**`方法，我们能够使用`tokenize.TabTokenizer()`方法基于单词串之间的标签从单词串中提取标记。

> **语法:** `tokenize.TabTokenizer()`
> **返回:**返回单词的代币。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`tokenize.TabTokenizer()`方法，我们能够从流中提取单词之间有制表符的标记。

```py
# import TabTokenizer() method from nltk
from nltk.tokenize import TabTokenizer

# Create a reference variable for Class TabTokenizer
tk = TabTokenizer()

# Create a string input
gfg = "Geeksfor\tGeeks..\t.$&* \nis\t for geeks"

# Use tokenize method
geek = tk.tokenize(gfg)

print(geek)
```

**输出:**

> [“极客”，“极客”, '.$&* \nis '，'针对极客']

**例 2 :**

```py
# import TabTokenizer() method from nltk
from nltk.tokenize import TabTokenizer

# Create a reference variable for Class TabTokenizer
tk = TabTokenizer()

# Create a string input
gfg = "The price\t of burger \tin BurgerKing is Rs.36.\n"

# Use tokenize method
geek = tk.tokenize(gfg)

print(geek)
```

**输出:**

> [“汉堡的价格”是 36 卢比
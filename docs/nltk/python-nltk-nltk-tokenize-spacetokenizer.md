# Python NLTK | NLTK . tokenize . spacetokenizer()

> 原文:[https://www . geesforgeks . org/python-nltk-nltk-token ize-space token izer/](https://www.geeksforgeeks.org/python-nltk-nltk-tokenize-spacetokenizer/)

借助`**nltk.tokenize.SpaceTokenizer()**`方法，我们能够使用`tokenize.SpaceTokenizer()`方法基于单词串之间的空间从单词串中提取标记。

> **语法:** `tokenize.SpaceTokenizer()`
> **返回:**返回单词的代币。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`tokenize.SpaceTokenizer()`方法，我们能够从流中提取单词之间有空间的单词的标记。

```
# import SpaceTokenizer() method from nltk
from nltk.tokenize import SpaceTokenizer

# Create a reference variable for Class SpaceTokenizer
tk = SpaceTokenizer()

# Create a string input
gfg = "Geeksfor Geeks.. .$&* \nis\t for geeks"

# Use tokenize method
geek = tk.tokenize(gfg)

print(geek)
```

**输出:**

> [“极客”，“极客”, '.$&* '，\nis\t '，'代表'，'极客']

**例 2 :**

```
# import SpaceTokenizer() method from nltk
from nltk.tokenize import SpaceTokenizer

# Create a reference variable for Class SpaceTokenizer
tk = SpaceTokenizer()

# Create a string input
gfg = "The price\t of burger \nin BurgerKing is Rs.36.\n"

# Use tokenize method
geek = tk.tokenize(gfg)

print(geek)
```

**输出:**

> ['The '，' price\t '，' of '，' burger '，' nin '，' BurgerKing '，' is '，' Rs.36.\n']
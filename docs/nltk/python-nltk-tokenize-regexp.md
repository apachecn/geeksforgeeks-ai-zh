# python nltk | token ize . regexp()

> 原文:[https://www.geeksforgeeks.org/python-nltk-tokenize-regexp/](https://www.geeksforgeeks.org/python-nltk-tokenize-regexp/)

借助`**NLTK tokenize.regexp()**`模块，我们可以通过`RegexpTokenizer()`方法使用正则表达式从字符串中提取标记。

> **语法:** `tokenize.RegexpTokenizer()`
> **返回:** **使用正则表达式返回令牌数组**

**示例#1 :**
在本例中，我们使用`RegexpTokenizer()`方法借助正则表达式提取令牌流。

```
# import RegexpTokenizer() method from nltk
from nltk.tokenize import RegexpTokenizer

# Create a reference variable for Class RegexpTokenizer
tk = RegexpTokenizer('\s+', gaps = True)

# Create a string input
gfg = "I love Python"

# Use tokenize method
geek = tk.tokenize(gfg)

print(geek)
```

**输出:**

> ['我'，'爱'，' Python']

**例 2 :**

```
# import RegexpTokenizer() method from nltk
from nltk.tokenize import RegexpTokenizer

# Create a reference variable for Class RegexpTokenizer
tk = RegexpTokenizer('\s+', gaps = True)

# Create a string input
gfg = "Geeks for Geeks"

# Use tokenize method
geek = tk.tokenize(gfg)

print(geek)
```

**输出:**

> [“极客”，“为”，“极客”
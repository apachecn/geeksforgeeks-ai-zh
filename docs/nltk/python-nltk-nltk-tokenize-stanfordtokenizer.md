# python nltk | nltk . token ize . stanfortoken izer()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-nltk-nltk-token ize-stanfortoken izer/

借助`**nltk.tokenize.StanfordTokenizer()**`方法，我们可以使用`tokenize.StanfordTokenizer()`方法从字符串或数字中提取标记。它遵循**斯坦福**生成代币的标准。

> **语法:** `tokenize.StanfordTokenizer()`
> **返回:** **从一串字符或数字中返回代币。**

**示例#1 :**
在这个示例中，我们可以看到，通过使用`tokenize.SExprTokenizer()`方法，我们能够使用斯坦福标准从字符或数字流中提取令牌。

```py
# import StanfordTokenizer() method from nltk
from nltk.tokenize.stanford import StanfordTokenizer

# Create a reference variable for Class StanfordTokenizer
tk = StanfordTokenizer()

# Create a string input
gfg = "Geeks f o r Geeks"

# Use tokenize method
geek = tk.tokenize(gfg)

print(geek)
```

**输出:**

> ['极客'，' f '，' o '，' r '，'极客'

**例 2 :**

```py
# import StanfordTokenizer() method from nltk
from nltk.tokenize.stanford import StanfordTokenizer

# Create a reference variable for Class StanfordTokenizer
tk = StanfordTokenizer()

# Create a string input
gfg = "This is your great author."

# Use tokenize method
geek = tk.tokenize(gfg)

print(geek)
```

**输出:**

> ['这'，'是'，'你的'，'伟大的'，'作者'，']
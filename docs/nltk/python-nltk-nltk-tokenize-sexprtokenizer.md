# python nltk | nltk . token ize . experimental izer()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-nltk-nltk-token ize-experts izer/

借助`**nltk.tokenize.SExprTokenizer()**`方法，我们可以使用`tokenize.SExprTokenizer()`方法从字符串或数字中提取标记。它实际上是在寻找合适的括号来制作标记。

> **语法:** `tokenize.SExprTokenizer()`
> **返回:**从一串字符或数字中返回令牌。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`tokenize.SExprTokenizer()`方法，我们能够通过考虑括号来从字符或数字流中提取标记。

```
# import SExprTokenizer() method from nltk
from nltk.tokenize import SExprTokenizer

# Create a reference variable for Class SExprTokenizer
tk = SExprTokenizer()

# Create a string input
gfg = "( a * ( b + c ))ab( a-c )"

# Use tokenize method
geek = tk.tokenize(gfg)

print(geek)
```

**输出:**

> ['( a * ( b+c))'，' ab '，'(a-c )']

**例 2 :**

```
# import SExprTokenizer() method from nltk
from nltk.tokenize import SExprTokenizer

# Create a reference variable for Class SExprTokenizer
tk = SExprTokenizer()

# Create a string input
gfg = "(a b) c d (e f)"

# Use tokenize method
geek = tk.tokenize(gfg)

print(geek)
```

**输出:**

> ['(a)b '，' c '，' d '，'(e)f ']
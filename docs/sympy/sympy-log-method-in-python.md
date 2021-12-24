# Python 中的 sympy.log()方法

> 原文:[https://www.geeksforgeeks.org/sympy-log-method-in-python/](https://www.geeksforgeeks.org/sympy-log-method-in-python/)

借助 **sympy.log()** 函数，我们可以简化自然对数的主分支。对数是用自然底数取的，例如，要得到不同底数 b 的对数，使用 log(x，y)，这实际上是 log(x) / log(y)的简称。

> **语法:** sympy.log()
> 
> **返回:**返回简化的数学表达式。

**示例#1 :**

## 蟒蛇 3

```
# import sympy 
from sympy import *

# Use sympy.log() method 
gfg = log(16, 2)

print(gfg)
```

**输出:**

```
4

```

**例 2 :**

## 蟒蛇 3

```
# import sympy 
from sympy import *

# Use sympy.log() method 
gfg = log(S(8) / 3, 2)

print(gfg)
```

**输出:**

```
- log(3)/log(2) + 3

```
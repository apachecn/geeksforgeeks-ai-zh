# Python | sympy.prod()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-prod-method/](https://www.geeksforgeeks.org/python-sympy-prod-method/)

借助`**sympy.prod()**`方法，我们可以找到两个整数的乘积，或者我们可以将列表与整数相乘，它将使用`sympy.prod()`方法返回列表中乘积的总和。

> **语法:** `sympy.prod(val1, val2)`
> **返回:**返回数字的乘积。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.prod()`方法，我们能够找到两个整数的乘积，并且我们能够找到 list 和整数的乘积，然后它将返回乘积的和。

```
# import sympy
from sympy import *

# Using sympy.prod() method
gfg = prod([1, 2, 3], 5)

print(gfg)
```

**输出:**

> Thirty

**例 2 :**

```
# import sympy
from sympy import *

# Using sympy.prod() method
gfg = prod(range(1, 5))

print(gfg)
```

**输出:**

> Twenty-four
# Python | sympy.csc()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-csc-method/](https://www.geeksforgeeks.org/python-sympy-csc-method/)

借助`**sympy.csc()**`方法，我们可以利用`sympy.csc()`函数求出余弦θ的值。

> **语法:** `sympy.csc()`
> **返回:**余弦θ的返回值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.csc()`方法，我们可以找到余弦θ的值。

```py
# import sympy
from sympy import *

# Use sympy.csc() method
gfg = simplify(csc(pi / 3))

print(gfg)
```

**输出:**

> 2*sqrt(3)/3

**例 2 :**

```py
# import sympy
from sympy import *

# Use sympy.csc() method
gfg = simplify(csc(pi / 4))

print(gfg)
```

**输出:**

> sqrt(2)
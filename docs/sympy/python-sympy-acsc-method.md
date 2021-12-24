# Python | sympy.acsc()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-acsc-method/](https://www.geeksforgeeks.org/python-sympy-acsc-method/)

借助`**sympy.acsc()**`方法，我们能够利用`sympy.acsc()`函数求出余弦倒数的值。

> **语法:** `sympy.acsc()`
> **返回:**余弦逆的返回值。

**示例#1 :**
在这个示例中我们可以看到，通过使用`sympy.acsc()`方法，我们可以找到余弦倒数的值。

```py
# import sympy
from sympy import *

# Use sympy.acsc() method
gfg = simplify(acsc(0.5))

print(gfg)
```

**输出:**

> 1.5707963267949–1.31695799696

**例 2 :**

```py
# import sympy
from sympy import *

# Use sympy.acsc() method
gfg = simplify(acsc(0.8))

print(gfg)
```

**输出:**

> 1.5707963267949–0.69314185945
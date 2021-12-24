# Python | sympy .拆开()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-apart-method/](https://www.geeksforgeeks.org/python-sympy-apart-method/)

借助`**sympy.apart()**`方法，我们能够对有理函数进行部分分式分解，并将其转化为标准范式，即`p/q`。

> **语法:** `sympy.apart()`
> **返回:**返回有理函数的部分分式分解。

**示例#1 :**
在给定的示例中，我们可以看到，通过使用`sympy.apart()`方法，我们可以做有理函数的部分分式。

```
# import sympy
from sympy import * x, y, z = symbols('x y z')
gfg_exp = (x**2 + 2 * x + 1)/(x**2 + x)

# Using sympy.apart() method
gfg_exp = apart(gfg_exp)

print(gfg_exp)
```

**输出:**

> 1 + 1/x

**例 2 :**

```
# import sympy
from sympy import * x, y, z = symbols('x y z')
gfg_exp = 1 / x + (3 * x / 2 - 2)/(x - 4)

# Using sympy.apart() method
gfg_exp = apart(gfg_exp)

print(gfg_exp)
```

**输出:**

> 3/2+4/(x–4)+1/x
# Python | sympy.cancel()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-cancel-method/](https://www.geeksforgeeks.org/python-sympy-cancel-method/)

借助`**sympy.cancel()**`方法，我们能够将任意有理函数化为标准范式，即`p/q`。

> **语法:** `sympy.cancel()`
> **返回:**返回任意有理函数的正则表达式。

**示例#1 :**
在给定的示例中，我们可以看到，通过使用`sympy.cancel()`方法，我们可以找到任意有理数的范式，即(p/q)。

```py
# import sympy
from sympy import * x, y, z = symbols('x y z')
gfg_exp = (x**2 + 2 * x + 1)/(x**2 + x)

# Using sympy.collect() method
gfg_exp = cancel(gfg_exp)

print(gfg_exp)
```

**输出:**

> (x + 1)/x

**例 2 :**

```py
# import sympy
from sympy import * x, y, z = symbols('x y z')
gfg_exp = 1 / x + (3 * x / 2 - 2)/(x - 4)

# Using sympy.collect() method
gfg_exp = cancel(gfg_exp)

print(gfg_exp)
```

**输出:**

> (3 * x * * 2–2 * x–8)/(2 * x * * 2–8 * x)
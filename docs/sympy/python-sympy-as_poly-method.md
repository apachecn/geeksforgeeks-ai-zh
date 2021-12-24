# Python | sympy.as_poly()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-as_poly-method/](https://www.geeksforgeeks.org/python-sympy-as_poly-method/)

借助`**sympy.as_poly()**`方法，我们可以利用`sympy.as_poly()`方法将数学函数变成多项式对象。

> **语法:** `sympy.as_poly()`
> **返回:**返回多项式对象。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.as_poly()`方法，我们能够从数学运算中获得多项式。

```py
# import sympy
from sympy import *

# Use sympy.as_poly() method
x = symbols('x')
gfg = (x**2 + 4 * x + 16).as_poly()

print(gfg)
```

**输出:**

> Poly(x**2 + 4*x + 16，x，domain='ZZ ')

**例 2 :**

```py
# import sympy
from sympy import *

# Use sympy.as_poly() method
x = symbols('x')
gfg = (x + 5 * x + 6).as_poly()

print(gfg)
```

**输出:**

> Poly(6*x + 6，x，domain='ZZ ')
# Python | sympy。Mod()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-mod-method/](https://www.geeksforgeeks.org/python-sympy-mod-method/)

借助`**sympy.Mod()**`方法，我们可以求出模量，并可以使用`sympy.Mod()`方法分别给出参数。

> **语法:** `sympy.Mod(var1, var2)`
> **返回:**返回模值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.Mod()`方法，我们能够找到给定参数的模数。

```py
# import sympy
from sympy import * 

x, y = symbols('x y')

# Using sympy.Mod() method
gfg = Mod(x, y).subs({x:7, y:2})

print(gfg)
```

**输出:**

> one

**例 2 :**

```py
# import sympy
from sympy import * 

x, y = symbols('x y')

# Using sympy.Mod() method
gfg = Mod(x**2, y).subs({x:7, y:5})

print(gfg)
```

**输出:**

> four
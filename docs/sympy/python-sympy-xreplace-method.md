# Python | sympy.xreplace()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-xreplace-method/](https://www.geeksforgeeks.org/python-sympy-xreplace-method/)

借助`**sympy.xreplace()**`方法，我们可以用数学表达式中函数的任何其他变量替换变量 x，而不用使用`sympy.xreplace()`方法编辑整个表达式。

> **语法:** `sympy.xreplace()`
> **返回:**返回数学表达式中 x 的替换值。

**示例#1 :**
在这个示例中我们可以看到，通过使用`sympy.xreplace()`方法，我们能够替换表达式中数学函数的 x 变量，并返回更新后的表达式。

```
# import sympy
from sympy import * 

x, y = symbols('x y')

f = sin(x) + cos(2 * x)
# Use sympy.xreplace() method
gfg = f.xreplace({2 * x : y})

print(gfg)
```

**输出:**

> sin(x) + cos(y)

**例 2 :**

```
# import sympy
from sympy import * 

x, y = symbols('x y')

f = log(sin(x)) + tan(cos(2 * x))
# Use sympy.xreplace() method
gfg = f.xreplace({ x : 2 * y})

print(gfg)
```

**输出:**

> log(sin(2*y)) + tan(cos(4*y))
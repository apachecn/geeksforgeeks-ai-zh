# Python | sympy.solve()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-solve-method/](https://www.geeksforgeeks.org/python-sympy-solve-method/)

借助`**sympy.solve(expression)**`方法，我们可以很容易地求解数学方程，它将返回使用`sympy.solve()`方法作为参数提供的方程的根。

> **语法:** `sympy.solve(expression)`
> **返回:**返回方程的根。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.solve()`方法，我们可以求解数学表达式，这将返回该方程的根。

```
# import sympy
from sympy import *

x, y = symbols('x y')
gfg_exp = x**2 - 4

print("Before Integration : {}".format(gfg_exp))

# Use sympy.integrate() method
intr = solve(gfg_exp, x)

print("After Integration : {}".format(intr))
```

**输出:**

> 集成前:x * * 2–4
> 
> 整合后:[-2，2]

**例 2 :**

```
# import sympy
from sympy import * 

x, y = symbols('x y')
gfg_exp = x**2 + 36

print("Before Integration : {}".format(gfg_exp))

# Use sympy.integrate() method
intr = solve(gfg_exp, x)

print("After Integration : {}".format(intr))
```

**输出:**

> 集成前:x**2 + 36
> 
> 整合后:[-6*I，6*I]
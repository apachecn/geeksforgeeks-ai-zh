# Python | sympy.series()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-series-method/](https://www.geeksforgeeks.org/python-sympy-series-method/)

借助`**sympy.series()**`方法，我们可以用`sympy.series()`方法求出一些数学函数和三角表达式的级数。

> **语法:** `sympy.series()`
> 
> **返回:**返回一系列功能。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.series()`方法，我们能够找到一些三角函数的级数。

```py
# import sympy
from sympy import * 

x, y = symbols('x y')

# Use sympy.series() method
gfg = cos(x).series()

print(gfg)
```

**输出:**

> 1–x * * 2/2+x * * 4/24+O(x * * 6)

**例 2 :**

```py
# import sympy
from sympy import * 

x, y = symbols('x y')

# Use sympy.series() method
gfg = tan(x).series()

print(gfg)
```

**输出:**

> x + x**3/3 + 2*x**5/15 + O(x**6)
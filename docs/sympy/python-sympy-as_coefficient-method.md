# Python | sympy.as_coefficient()方法

> 原文:[https://www . geesforgeks . org/python-sympy-as _ coefficient-method/](https://www.geeksforgeeks.org/python-sympy-as_coefficient-method/)

借助`**sympy.as_coefficient()**`方法，我们可以用`sympy.as_coefficient()`方法求出数学表达式中任意元素的系数。

> **语法:** `sympy.as_coefficient()`
> **返回:**返回任意元素的系数。

**例#1 :**
在这里我们可以看到，通过使用`sympy.as_coefficient()`方法，我们能够得到作为参数传递的任何元素的系数值。

```
# import sympy
from sympy import * 

x = symbols('x')

# Use sympy.as_coefficient() method
gfg = x**3 + 21 * x + 12

print(gfg.as_coefficient(x))
```

**输出:**

> Twenty-one

**例 2 :**

```
# import sympy
from sympy import * 

x = symbols('x')

# Use sympy.as_coefficient() method
gfg = x**3 + 21 * x**2 + 121x + 4

print(gfg.as_coefficient(x))
```

**输出:**

> One hundred and twenty-one
# Python | sympy . as _ leading _ term()方法

> 原文:[https://www . geesforgeks . org/python-sympy-as _ leading _ term-method/](https://www.geeksforgeeks.org/python-sympy-as_leading_term-method/)

借助`**sympy.as_leading_term()**`方法，我们可以看到在`sympy.as_leading_term()`方法中作为参数传递的变量的数学表达式中的前导项。

> **语法:** `sympy.as_leading_term(variable)`
> **返回:**返回前导项的函数或表达式。

**示例#1 :**
在本例中我们可以看到，通过使用`sympy.as_leading_term()`方法，我们能够检查作为参数传递的变量的数学函数的前导项。

```
# import sympy
from sympy import * 

x, y = symbols('x y')

# Use sympy.as_leading_term(variable) method
gfg = (x**2 + 2 * x*y + y**2).as_leading_term(y)

print(gfg)
```

**输出:**

> x**2

**例 2 :**

```
# import sympy
from sympy import * 

x, y = symbols('x y')

# Use sympy.as_leading_term(variable) method
gfg = (x * sin(x)*cos(y) + log(tan(x))).as_leading_term(y)

print(gfg)
```

**输出:**

> x*sin(x) + log(tan(x))
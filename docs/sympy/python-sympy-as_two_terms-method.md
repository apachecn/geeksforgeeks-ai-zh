# Python | sympy.as_two_terms()方法

> 原文:[https://www . geesforgeks . org/python-sympy-as _ two _ terms-method/](https://www.geeksforgeeks.org/python-sympy-as_two_terms-method/)

借助`**sympy.as_two_terms()**`方法，我们可以通过数学表达式中的**常量**值来分离数学表达式，并使用`sympy.as_two_terms()`方法返回一个元组。

> **语法:** `sympy.as_two_terms()`
> **返回:**返回由**常量**值分隔的元素元组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.as_two_terms()`方法，我们能够获得由**常量**值分隔的元素元组。

```py
# import sympy
from sympy import * 

x, y = symbols('x y')

# Using sympy.as_two_terms() method
gfg = (3 * x + 5 * y + 6).as_two_terms()

print(gfg)
```

**输出:**

> (6，3*x + 5*y)

**例 2 :**

```py
# import sympy
from sympy import * 

x, y = symbols('x y')

# Using sympy.as_two_terms() method
gfg = (x**2 + 4).as_two_terms()

print(gfg)
```

**输出:**

> (4，x**2)
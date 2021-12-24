# Python | sympy.primitive()方法

> 原文:[https://www . geesforgeks . org/python-sympy-primitive-method/](https://www.geeksforgeeks.org/python-sympy-primitive-method/)

借助`**sympy.primitive()**`方法，我们可以用`sympy.primitive()`方法找到一个数学表达式的公共部分。

> **语法:** `sympy.primitive()`
> **返回:**返回从数学表达式中分离出公共部分的元组。

**示例#1 :**
在这个示例中我们可以看到，通过使用`sympy.primitive()`方法，我们能够从数学表达式中找到公共部分。

```
# import sympy
from sympy import * 

x, y = symbols('x y')

# Using sympy.primitive() method
gfg = (3 * x + 9 * y).primitive()

print(gfg)
```

**输出:**

> (3，x + 3*y)

**例 2 :**

```
# import sympy
from sympy import * 

x, y = symbols('x y')

# Using sympy.primitive() method
gfg = (2 * x / 7 + 4 * y / 14).primitive()

print(gfg)
```

**输出:**

> (2/7，x + y)
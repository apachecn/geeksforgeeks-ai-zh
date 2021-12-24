# Python | sympy . is _ 代数方法

> 原文:[https://www . geesforgeks . org/python-sympy-is _ 代数-method/](https://www.geeksforgeeks.org/python-sympy-is_algebraic-method/)

借助`**sympy.is_algebraic**`方法，我们可以检查天气元素是否是代数元素，该方法将返回布尔值，即真或假。

> **语法:** `sympy.is_algebraic`
> **返回:**如果代数否则返回真假。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.is_algebraic`方法，我们能够检查代数值，它将返回一个布尔值。

```py
# import sympy
from sympy import * 

x = symbols('x')

# Use sympy.is_algebraic method
gfg = simplify(2 * x).is_algebraic

print(gfg)
```

**输出:**

> 真实的

**例 2 :**

```py
# import sympy
from sympy import *

# Use sympy.is_algebraic method
gfg = simplify(5I).is_algebraic

print(gfg)
```

**输出:**

> 错误的
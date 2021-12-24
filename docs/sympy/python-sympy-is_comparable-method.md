# Python | sympy . is _ compatible()方法

> 原文:[https://www . geesforgeks . org/python-sympy-is _ compatible-method/](https://www.geeksforgeeks.org/python-sympy-is_comparable-method/)

借助`**sympy.is_comparable()**`方法，我们可以精确计算实数，如果计算值是精确实数，则使用`sympy.is_comparable()`方法返回真。

> **语法:** `sympy.is_comparable()`
> **返回:**计算实数时返回布尔值。

**示例#1 :**
在本例中，我们可以看到，通过使用`sympy.is_comparable()`方法，我们能够评估表达式，如果计算值是精确的实数，它将返回真或假。

```py
# import sympy
from sympy import * 

x, y, z = symbols('x y z')

# Use sympy.is_comparable() method
gfg = (3 * x + 2 * tan(y + I * pi) + log(2 * x)).is_comparable

print(gfg)
```

**输出:**

> 错误的

**例 2 :**

```py
# import sympy
from sympy import * 

x, y, z = symbols('x y z')

# Use sympy.is_comparable() method
gfg = (pi / 2).is_comparable

print(gfg)
```

**输出:**

> 真实的
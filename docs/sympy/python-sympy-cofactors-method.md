# Python | sympy.cofactors()方法

> 原文:[https://www . geesforgeks . org/python-sympy-辅因子-method/](https://www.geeksforgeeks.org/python-sympy-cofactors-method/)

借助`**sympy.cofactors()**`方法，我们可以找到在`sympy.cofactors()`方法中作为参数传递的两个数的辅因子。

> **语法:** `sympy.cofactors(var1, var2)`
> **返回:**返回辅因子元组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.cofactors()`方法，我们能够找到作为参数传递的任意两个数字的辅因子。

```py
# import sympy
from sympy import *

# Using sympy.cofactors() method
gfg = cofactors(6, 8)

print(gfg)
```

**输出:**

> ( 2, 3, 4 )

**例 2 :**

```py
# import sympy
from sympy import *

# Using sympy.cofactors() method
gfg = cofactors(34, 81)

print(gfg)
```

**输出:**

> ( 1, 34, 81 )
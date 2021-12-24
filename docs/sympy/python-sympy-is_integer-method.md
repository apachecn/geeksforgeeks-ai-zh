# Python | sympy.is_integer 方法

> 原文:[https://www . geesforgeks . org/python-sympy-is _ integer-method/](https://www.geeksforgeeks.org/python-sympy-is_integer-method/)

借助`**sympy.is_integer**`方法，我们可以检查天气元素是否为整数，该方法将返回布尔值，即真或假。

> **语法:** `sympy.is_integer`
> **返回:**如果整数否则返回真假。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.is_integer`方法，我们能够检查整数值，它将返回一个布尔值。

```
# import sympy
from sympy import *

# Use sympy.is_integer method
gfg = simplify(2).is_integer

print(gfg)
```

**输出:**

> 真实的

**例 2 :**

```
# import sympy
from sympy import *

# Use sympy.is_integer method
gfg = simplify(5.5).is_integer

print(gfg)
```

**输出:**

> 错误的
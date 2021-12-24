# Python | sympy.is_composite 方法

> 原文:[https://www . geesforgeks . org/python-sympy-is _ composite-method/](https://www.geeksforgeeks.org/python-sympy-is_composite-method/)

借助`**sympy.is_composite**`方法，我们可以检查天气元素是否合成，该方法将返回布尔值，即真或假。

> **语法:** `sympy.is_composite`
> **返回:**复合否则返回真假。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.is_composite`方法，我们能够检查复合值，它将返回一个布尔值。

```
# import sympy
from sympy import *

# Use sympy.is_composite method
gfg = simplify(6).is_composite

print(gfg)
```

**输出:**

> 真实的

**例 2 :**

```
# import sympy
from sympy import *

# Use sympy.is_composite method
gfg = simplify(3).is_composite

print(gfg)
```

**输出:**

> 错误的
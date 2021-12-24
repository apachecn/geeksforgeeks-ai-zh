# Python | sympy . is _ 虚数法

> 原文:[https://www . geesforgeks . org/python-sympy-is _ imaginal-method/](https://www.geeksforgeeks.org/python-sympy-is_imaginary-method/)

借助`**sympy.is_imaginary**`方法，我们可以检查天气元素是否是虚的，该方法将返回布尔值，即真或假。

> **语法:** `sympy.is_imaginary`
> **返回:**若虚则返回真否则返回假。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.is_imaginary`方法，我们能够检查虚数，它将返回一个布尔值。

```
# import sympy
from sympy import *

# Use sympy.is_imaginary method
gfg = simplify(2 * I).is_imaginary

print(gfg)
```

**输出:**

> 真实的

**例 2 :**

```
# import sympy
from sympy import *

# Use sympy.is_imaginary method
gfg = simplify(5).is_imaginary

print(gfg)
```

**输出:**

> 错误的
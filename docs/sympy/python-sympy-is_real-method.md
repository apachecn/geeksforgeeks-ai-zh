# Python | sympy.is_real 方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-is_real-method/](https://www.geeksforgeeks.org/python-sympy-is_real-method/)

借助`**sympy.is_real**`方法，我们可以检查天气元素是否真实，该方法将返回布尔值，即真或假。

> **语法:** `sympy.is_real`
> **返回:**真则返回真否则返回假。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.is_real`方法，我们能够检查真实值，它将返回一个布尔值。

```
# import sympy
from sympy import *

# Use sympy.is_real method
gfg = simplify(2).is_real

print(gfg)
```

**输出:**

> 真实的

**例 2 :**

```
# import sympy
from sympy import *

# Use sympy.is_real method
gfg = simplify(5.5).is_real

print(gfg)
```

**输出:**

> 真实的
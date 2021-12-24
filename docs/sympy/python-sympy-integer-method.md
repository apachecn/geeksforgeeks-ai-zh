# Python | sympy。整数()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-integer-method/](https://www.geeksforgeeks.org/python-sympy-integer-method/)

借助`**sympy.Integer()**`方法，我们可以将浮点转换为整数值，如果我们想保存整数值，这种方法在内存方面非常有效。

> **语法:** `sympy.Integer()`
> **返回:**返回整数值。

**示例#1 :**
在这个示例中，我们可以看到通过使用`sympy.Integer()`方法，我们能够将浮点值转换为整数或优化内存消耗。

```py
# import sympy
from sympy import *

# Use sympy.Integer() method
gfg = Integer(50) + Integer(50)

print(gfg)
```

**输出:**

> One hundred

**例 2 :**

```py
# import sympy
from sympy import *

# Use sympy.Integer() method
gfg = Integer(12.36) + Integer(8.98)

print(gfg)
```

**输出:**

> Twenty
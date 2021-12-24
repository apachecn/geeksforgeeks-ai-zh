# Python | sympy。浮动()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-float-method/](https://www.geeksforgeeks.org/python-sympy-float-method/)

借助`**sympy.Float()**`方法，我们可以将整数值转换为浮点值，并且通过使用该方法，我们还可以设置精度值。默认情况下，精度值为 15。

> **语法:** `sympy.Float()`
> **返回:**返回浮点数。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.Float()`方法，我们可以将整数值精确地转换为浮点值。

```
# import sympy
from sympy import *

# Use sympy.Float() method
gfg = Float(56)

print(gfg)
```

**输出:**

> 56.0000000000000

**例 2 :**

```
# import sympy
from sympy import *

# Use sympy.Float() method
gfg = Float(456, 6)

print(gfg)
```

**输出:**

> Four hundred and fifty-six
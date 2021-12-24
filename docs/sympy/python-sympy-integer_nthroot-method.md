# Python | sympy . integer _ n throot()方法

> 原文:[https://www . geeksforgeeks . org/python-sympy-integer _ n throot-method/](https://www.geeksforgeeks.org/python-sympy-integer_nthroot-method/)

借助`**sympy.integer_nthroot()**`方法，我们可以找到在`sympy.integer_nthroot()`方法中作为参数传递的数字的第 n 个根。它将返回一个有两个值的元组，一个是根，另一个是布尔值，它显示根是否完美。

> **语法:** `sympy.integer_nthroot(val)`
> **返回:**返回具有根和布尔值的元组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`integer_nthroot()`方法，我们能够找到作为参数传递的数字的第 n 个根。

```
# import sympy
from sympy import *

# Using sympy.integer_nthroot() method
gfg = integer_nthroot(25, 2)

print(gfg)
```

**输出:**

```
(5, True)

```

**例 2 :**

```
# import sympy
from sympy import *

# Using sympy.integer_nthroot() method
gfg = integer_nthroot(80, 3)

print(gfg)
```

**输出:**

```
(4, False)

```
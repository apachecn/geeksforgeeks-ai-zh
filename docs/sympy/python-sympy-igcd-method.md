# Python | sympy.igcd()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-igcd-method/](https://www.geeksforgeeks.org/python-sympy-igcd-method/)

借助`**sympy.igcd()**`方法，我们可以找到在`sympy.igcd()`方法中作为参数传递的两个非负整数的最大公约数。

> **语法:** `sympy.igcd(var1, var2)`
> **返回:**非负整数最大公约数的返回值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.igcd()`方法，我们能够找到作为参数传递的任意两个非负数的最大公约数。

```
# import sympy
from sympy import *

# Using sympy.igcd() method
gfg = igcd(45, 35)

print(gfg)
```

**输出:**

> five

**例 2 :**

```
# import sympy
from sympy import *

# Using sympy.igcd() method
gfg = igcd(17, 19)

print(gfg)
```

**输出:**

> one
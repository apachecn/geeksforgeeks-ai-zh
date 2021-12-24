# Python | sympy.ilcm()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-ilcm-method/](https://www.geeksforgeeks.org/python-sympy-ilcm-method/)

借助`**sympy.ilcm()**`方法，我们可以找到在`sympy.ilcm()`方法中作为参数传递的两个非负整数的最小公倍数。

> **语法:** `sympy.ilcm(var1, var2)`
> **返回:**两个非负整数的最小公倍数的返回值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.ilcm()`方法，我们能够找到作为参数传递的任意两个非负整数的最小公倍数。

```py
# import sympy
from sympy import *

# Using sympy.ilcm() method
gfg = ilcm(2, 3)

print(gfg)
```

**输出:**

```py
6

```

**例 2 :**

```py
# import sympy
from sympy import *

# Using sympy.ilcm() method
gfg = ilcm(7, 6)

print(gfg)
```

**输出:**

```py
42

```
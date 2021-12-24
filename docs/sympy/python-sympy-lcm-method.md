# Python | sympy.lcm()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-lcm-method/](https://www.geeksforgeeks.org/python-sympy-lcm-method/)

借助`**sympy.lcm()**`方法，我们可以找到在`sympy.lcm()`方法中作为参数传递的两个数的最小公倍数。

> **语法:** `sympy.lcm(var1, var2)`
> **返回值:**最小公倍数的返回值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.lcm()`方法，我们能够找到作为参数传递的任意两个数字的最小公倍数。

```py
# import sympy
from sympy import *

# Using sympy.lcm() method
gfg = lcm(61, 24)

print(gfg)
```

**输出:**

> One thousand four hundred and sixty-four

**例 2 :**

```py
# import sympy
from sympy import *

# Using sympy.lcm() method
gfg = lcm(17, 16)

print(gfg)
```

**输出:**

> Two hundred and seventy-two
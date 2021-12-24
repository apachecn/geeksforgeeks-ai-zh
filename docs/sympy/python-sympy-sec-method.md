# Python | sympy.sec()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-sec-method/](https://www.geeksforgeeks.org/python-sympy-sec-method/)

借助`**sympy.sec()**`方法，我们能够利用`sympy.sec()`函数找到秒θ的值。

> **语法:** `sympy.sec()`
> **返回:**秒θ的返回值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.sec()`方法，我们可以找到秒θ的值。

```py
# import sympy
from sympy import *

# Use sympy.sec() method
gfg = simplify(sec(pi / 6))

print(gfg)
```

**输出:**

> 2*sqrt(3)/3

**例 2 :**

```py
# import sympy
from sympy import *

# Use sympy.sec() method
gfg = simplify(sec(pi / 3))

print(gfg)
```

**输出:**

> Two
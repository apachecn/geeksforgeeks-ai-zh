# Python | sympy.gcd()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-gcd-method/](https://www.geeksforgeeks.org/python-sympy-gcd-method/)

借助`**sympy.gcd()**`方法，我们可以找到在`sympy.gcd()`方法中作为参数传递的两个数的最大公约数。

> **语法:** `sympy.gcd(var1, var2)`
> **返回:**最大公约数返回值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.gcd()`方法，我们能够找到作为参数传递的任意两个数字的最大公约数。

```
# import sympy
from sympy import *

# Using sympy.gcd() method
gfg = gcd(6, 8)

print(gfg)
```

**输出:**

> Two

**例 2 :**

```
# import sympy
from sympy import *

# Using sympy.gcd() method
gfg = gcd(177, 81)

print(gfg)
```

**输出:**

> three
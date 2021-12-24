# Python | sympy.as_real_imag()方法

> 原文:[https://www . geesforgeks . org/python-sympy-as _ real _ imag-method/](https://www.geeksforgeeks.org/python-sympy-as_real_imag-method/)

借助`**sympy.as_real_imag()**`方法，利用`sympy.as_real_imag()`方法可以得到第一个值为实值，另一个值为虚值的元组。

> **语法:** `sympy.as_real_imag()`
> **返回:**返回一个既有实值又有虚值的元组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.as_real_imag()`方法，我们能够获得包含实值和虚值的元组。

```py
# import sympy
from sympy import *

# Using sympy.as_real_imag() method
gfg = (4 + 5 * I).as_real_imag()

print(gfg)
```

**输出:**

> (4, 5)

**例 2 :**

```py
# import sympy
from sympy import *

# Using sympy.as_real_imag() method
gfg = (5 + 10 * I -5 * I**2).as_real_imag()

print(gfg)
```

**输出:**

> (10, 10)
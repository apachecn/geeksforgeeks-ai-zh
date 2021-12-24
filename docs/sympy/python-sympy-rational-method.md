# Python | sympy。有理()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-rational-method/](https://www.geeksforgeeks.org/python-sympy-rational-method/)

借助`**sympy.Rational()**`方法，我们可以找到在`sympy.Rational()`方法中作为参数传递的任意浮点值的有理形式。

> **语法:** `sympy.Rational(val)`
> **返回:**返回理性形式的浮点值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.Rational()`方法，我们能够找到作为参数传递的任何浮点值的有理形式。

```
# import sympy
from sympy import *

# Using sympy.Rational() method
gfg = Rational(0.2)

print(gfg)
```

**输出:**

> 1/5

**例 2 :**

```
# import sympy
from sympy import *

# Using sympy.Rational() method
gfg = Rational(0.12)

print(gfg)
```

**输出:**

> 12/100
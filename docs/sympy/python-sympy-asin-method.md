# Python | sympy.asin()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-asin-method/](https://www.geeksforgeeks.org/python-sympy-asin-method/)

借助`**sympy.asin(x)**`方法，我们能够求出正弦θ的倒数。

> **语法:** `sympy.asin(x)`
> **返回:**返回逆正弦θ的值。

**示例#1 :**
在给定的示例中，我们可以看到，通过使用`sympy.asin(x)`方法，我们可以找到正弦θ的逆。

```
# import sympy
from sympy import * x, y, z = symbols('x y z')

# Using sympy.asin() method
gfg_exp = asin(1)

print(gfg_exp)
```

**输出:**

> pi/2

**例 2 :**

```
# import sympy
from sympy import * x, y, z = symbols('x y z')

# Using sympy.asin() method
gfg_exp = asin(1 / 2)

print(gfg_exp)
```

**输出:**

> 0.523598775598299
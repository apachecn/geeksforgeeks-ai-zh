# Python | sympy.acos(x)方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-acosx-method/](https://www.geeksforgeeks.org/python-sympy-acosx-method/)

借助`**sympy.acos(x)**`方法，我们能够求出余弦θ的倒数。

> **语法:** `sympy.acos(x)`
> **返回:**返回反余弦θ的值。

**示例#1 :**
在给定的示例中，我们可以看到，通过使用`sympy.acos(x)`方法，我们可以找到余弦θ的倒数。

```
# import sympy
from sympy import * x, y, z = symbols('x y z')

# Using sympy.acos() method
gfg_exp = acos(0)

print(gfg_exp)
```

**输出:**

> pi/2

**例 2 :**

```
# import sympy
from sympy import * x, y, z = symbols('x y z')

# Using sympy.acos() method
gfg_exp = acos(sqrt(3)/2)

print(gfg_exp)
```

**输出:**

> pi/6
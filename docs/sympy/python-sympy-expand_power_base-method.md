# Python | sympy . expand _ power _ base()方法

> 原文:[https://www . geesforgeks . org/python-sympy-expand _ power _ base-method/](https://www.geeksforgeeks.org/python-sympy-expand_power_base-method/)

借助`**sympy.expand_power_base()**`方法，我们可以用`sympy.expand_power_base()`方法简化数学表达式的幂。

> **语法:** `sympy.expand_power_base()`
> **返回:**返回使用 base 的简化数学表达式。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.expand_power_base()`方法，我们能够使用基数简化数学表达式的幂。

```py
# import sympy
from sympy import * 

x, y = symbols('x y')
gfg_exp = x**2 + 2 * x*y + y**2

# Use sympy.expand_power_base() method
fact = expand_power_base(gfg_exp)

print(fact)
```

**输出:**

> x**2 + 2*x*y + y**2

**例 2 :**

```py
# import sympy
from sympy import * 

x, y, z = symbols('x y z')
gfg_exp = x**(a + b)

# Use sympy.expand_power_base() method
fact = expand_power_base(gfg_exp)

print(fact)
```

**输出:**

> x**a*x**b
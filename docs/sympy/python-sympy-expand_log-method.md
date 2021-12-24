# Python | sympy.expand_log()方法

> 原文:[https://www . geesforgeks . org/python-sympy-expand _ log-method/](https://www.geeksforgeeks.org/python-sympy-expand_log-method/)

借助`**sympy.expand_log()**`，我们可以利用下面列出的下列性质，简化数学表达式中的对数项。

**属性:**
**1)**log(x * y)= log(x)+log(y)
**2)**log(x * * n)= nlog(x)

> **语法:** `sympy.expand_log()`
> **返回:**返回简化的数学表达式。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.expand_log()`，我们能够在数学表达式中简化对数项。

```py
# import sympy
from sympy import * 

x, y, z = symbols('x y z', positive = True)
gfg_exp = log(x * y)

# Using sympy.expand_log() method
gfg_exp = expand_log(gfg_exp)

print(gfg_exp)
```

**输出:**

> 对数(x) +对数(y)

**例 2 :**

```py
# import sympy
from sympy import * 

x, y, z = symbols('x y z', positive = True)
gfg_exp = log(x**3)

# Using sympy.expand_log() method
gfg_exp = expand_log(gfg_exp)

print(gfg_exp)
```

**输出:**

> 3*log(x)
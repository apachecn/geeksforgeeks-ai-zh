# Python | sympy.logcombine()方法

> 原文:[https://www . geesforgeks . org/python-sympy-log combine-method/](https://www.geeksforgeeks.org/python-sympy-logcombine-method/)

在`**sympy.logcombine()**`的帮助下，我们可以通过使用下面列出的以下属性来组合数学表达式中的对数项。

**属性:**
**1)**log(x * y)= log(x)+log(y)
**2)**log(x * * n)= nlog(x)

> **语法:** `sympy.logcombine()`
> 
> **返回:**返回简化的数学表达式。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.logcombine()`，我们能够在数学表达式中组合对数项。

```
# import sympy
from sympy import * 

x, y, z = symbols('x y z', positive = True)
gfg_exp = log(x) + log(y)

# Using sympy.logcombine() method
gfg_exp = logcombine(gfg_exp)

print(gfg_exp)
```

**输出:**

> 日志(x*y)

**例 2 :**

```
# import sympy
from sympy import * 

x, y, z = symbols('x y z', positive = True)
gfg_exp = 5 * log(x)

# Using sympy.logcombine() method
gfg_exp = logcombine(gfg_exp)

print(gfg_exp)
```

**输出:**

> 日志(x**5)
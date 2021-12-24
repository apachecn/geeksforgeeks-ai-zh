# Python | sympy.integrate()使用限制

> 原文:[https://www . geesforgeks . org/python-sympy-integrate-using-limits/](https://www.geeksforgeeks.org/python-sympy-integrate-using-limits/)

借助`**sympy.integrate(expression, limit)**`方法，我们可以通过`sympy.integrate(expression, limit)`方法找到以变量形式使用极限的数学表达式的积分。

> **语法:** `sympy.integrate(expression, reference variable, limit)`
> **返回:**返回积分的数学表达式。

**示例#1 :**

在这个例子中我们可以看到，通过使用`sympy.integrate(expression, limits)`方法，我们可以找到使用极限与变量的数学表达式的积分。这里我们也使用`symbols()`方法将变量声明为符号。

```
# import sympy
from sympy import * 

x, y = symbols('x y')
gfg_exp = cos(x)

print("Before Integration : {}".format(gfg_exp))

# Use sympy.integrate() method
intr = integrate(gfg_exp,  (x, -oo, oo))

print("After Integration : {}".format(intr))
```

**输出:**

> 集成前:cos(x)
> 
> 积分后:累计值(-2，2)

**例 2 :**

```
# import sympy
from sympy import * 

x, y = symbols('x y')
gfg_exp = tan(x)

print("Before Integration : {}".format(gfg_exp))

# Use sympy.integrate() method
intr = integrate(gfg_exp,  (x, -1, 1))

print("After Integration : {}".format(intr))
```

**输出:**

> 集成前:tan(x)
> 
> 集成后:0
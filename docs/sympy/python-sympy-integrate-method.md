# Python | sympy.integrate()方法

> 原文:[https://www . geesforgeks . org/python-sympy-integrate-method/](https://www.geeksforgeeks.org/python-sympy-integrate-method/)

借助`**sympy.integrate()**`方法，我们可以利用`sympy.integrate()`方法找到变量形式的数学表达式的积分。

> **语法:** `sympy.integrate(expression, reference variable)`
> **返回:**返回积分的数学表达式。

**示例#1 :**
在这个示例中我们可以看到，通过使用`sympy.integrate()`方法，我们可以找到数学表达式与变量的积分。这里我们也使用`symbols()`方法将变量声明为符号。

```
# import sympy
from sympy import * x, y = symbols('x y')
gfg_exp = sin(x)*exp(x)

print("Before Integration : {}".format(gfg_exp))

# Use sympy.integrate() method
intr = integrate(gfg_exp, x)

print("After Integration : {}".format(intr))
```

**输出:**

> 积分前:exp(x)*sin(x)
> 
> 积分后:exp(x)* sin(x)/2–exp(x)* cos(x)/2

**例 2 :**

```
# import sympy
from sympy import * x, y = symbols('x y')
gfg_exp = sin(x)*tan(x)

print("Before Integration : {}".format(gfg_exp))

# Use sympy.integrate() method
intr = integrate(gfg_exp, x)

print("After Integration : {}".format(intr))
```

**输出:**

> 积分前:sin(x)*tan(x)
> 
> 积分后:-对数(正弦(x)–1)/2+对数(正弦(x)+1)/2–正弦(x)
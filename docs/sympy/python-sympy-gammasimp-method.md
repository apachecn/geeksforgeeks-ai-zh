# Python | sympy.gammasimp()方法

> 原文:[https://www . geesforgeks . org/python-sympy-gammasimp-method/](https://www.geeksforgeeks.org/python-sympy-gammasimp-method/)

借助 **sympy.gammasimp()** 方法，我们可以用 gamma 函数或非整数变元的组合函数来简化表达式

> **语法:** gammasimp(表达式)
> 
> **参数:**
> **表达式–**是需要简化的数学表达式。
> 
> **返回:**返回与输入对应的简化数学表达式。

**示例#1:**

```py
# import sympy 
from sympy import * x = symbols('x')
expr = gamma(x)*gamma(1 - x)
print("Expression = {}".format(expr))

# Use sympy.gammasimp() method 
simple_expr = gammasimp(expr)  

print("Simplified Expression : {}".format(simple_expr))  
```

**输出:**

```py
Expression = gamma(x)*gamma(1 - x)
Simplified Expression : pi/sin(pi*x)

```

**例 2:**

```py
# import sympy 
from sympy import * x = symbols('x')
expr = gamma(x + 1)/gamma(x - 1)
print("Expression = {}".format(expr))

# Use sympy.gammasimp() method 
simple_expr = gammasimp(expr)  

print("Simplified Expression : {}".format(simple_expr))  
```

**输出:**

```py
Expression = gamma(x + 1)/gamma(x - 1)
Simplified Expression : x*(x - 1)

```
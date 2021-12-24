# Python | sympy.simplify()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-simplify-method/](https://www.geeksforgeeks.org/python-sympy-simplify-method/)

借助 **sympy.simplify()** 方法，我们可以简化任何数学表达式。

> **语法:**简化(表达式)
> 
> **参数:**
> **表达式**——是需要简化的数学表达式。
> 
> **返回:**返回与输入表达式对应的简化数学表达式。

**示例#1:**
在这个示例中，我们可以看到，通过使用 **sympy.lambdify()** 方法，我们可以简化任何数学表达式。

```py
# import sympy
from sympy import * 

x = symbols('x')
expr = sin(x)**2 + cos(x)**2

print("Before Simplification : {}".format(expr))

# Use sympy.simplify() method
smpl = simplify(expr) 

print("After Simplification : {}".format(smpl)) 
```

**输出:**

```py
Before Simplification : sin(x)**2 + cos(x)**2
After Simplification : 1

```

**例 2:**

```py
# import sympy
from sympy import * 

x = symbols('x')
expr = (x**3 + x**2 - x - 1)/(x**2 + 2 * x + 1)

print("Before Simplification : {}".format(expr))

# Use sympy.simplify() method
smpl = simplify(expr) 

print("After Simplification : {}".format(smpl)) 
```

**输出:**

```py
Before Simplification : (x**3 + x**2 - x - 1)/(x**2 + 2*x + 1)
After Simplification : After Simplification : x - 1

```
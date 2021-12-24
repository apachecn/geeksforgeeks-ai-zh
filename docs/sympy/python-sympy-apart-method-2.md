# Python | sympy .拆开()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-apart-method-2/](https://www.geeksforgeeks.org/python-sympy-apart-method-2/)

借助 **sympy .拆开()**方法，我们可以对一个有理数学表达式进行部分分式分解。

> **语法:**分开(表达式)
> 
> **参数:**
> **表达式**——是一个理性的数学表达式。
> 
> **返回:**返回部分分解后的表达式。

**例#1:**
在这个例子中我们可以看到，通过使用 **sympy .拆开()**方法，我们可以得到给定数学表达式的部分分数分解。

```py
# import sympy
from sympy import *

x = symbols('x')
expr = (4 * x**3 + 21 * x**2 + 10 * x + 12) / (x**4 + 5 * x**3 + 5 * x**2 + 4 * x)

print("Mathematical expression : {}".format(expr))

# Use sympy.apart() method
pd = apart(expr) 

print("After Partial Decomposition : {}".format(pd)) 
```

**输出:**

```py
Mathematical expression : (4*x**3 + 21*x**2 + 10*x + 12)/(x**4 + 5*x**3 + 5*x**2 + 4*x)
After Partial Decomposition : (2*x - 1)/(x**2 + x + 1) - 1/(x + 4) + 3/x

```

**例 2:**

```py
# import sympy
from sympy import * 

x = symbols('x')
expr = 1/(x + 3)(x + 2)

print("Mathematical expression : {}".format(expr))

# Use sympy.factor_list() method
pd = apart(expr) 

print("After Partial Decomposition : {}".format(pd)) 
```

**输出:**

```py
Mathematical expression : 1/((x + 2)*(x + 3))
After Partial Decomposition : -1/(x + 3) + 1/(x + 2)

```
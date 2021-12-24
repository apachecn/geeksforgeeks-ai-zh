# Python | sympy . powsim()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-powsimp-method/](https://www.geeksforgeeks.org/python-sympy-powsimp-method/)

借助于**sympy . powsim()**方法，我们可以利用涉及幂的指数定律简化数学表达式。

**属性:**
1)x * * a * x * * b = x * *(a+b)
2)x * * a * y * * a =(xy)* * a

> **语法:** powsimp(表达式)
> 
> **参数:**
> **表达式**——是需要简化的数学表达式。
> 
> **返回:**返回与输入表达式对应的简化数学表达式。

**例#1:**
在这个例子中我们可以看到，通过使用**sympy . powsim()**方法，我们可以使用涉及幂的指数定律来简化任何数学表达式。

```py
# import sympy
from sympy import * 

x, a, b = symbols('x a b')
expr = x**a * x**b

print("Before Simplification : {}".format(expr))

# Use sympy.powsimp() method
smpl = powsimp(expr) 

print("After Simplification : {}".format(smpl)) 
```

**输出:**

```py
Before Simplification : x**a*x**b
After Simplification : x**(a + b)

```

**例 2:**

```py
# import sympy
from sympy import * 

x, a, b = symbols('x a b')
expr = ((x**(2 * a + b))*(x**(-a + b)))

print("Before Simplification : {}".format(expr))

# Use sympy.powsimp() method
smpl = powsimp(expr) 

print("After Simplification : {}".format(smpl)) 
```

**输出:**

```py
Before Simplification : x**(-a + b)*x**(2*a + b)
After Simplification : x**(a + 2*b)

```
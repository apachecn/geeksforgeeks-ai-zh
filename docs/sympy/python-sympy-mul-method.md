# Python | sympy。Mul()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-mul-method/](https://www.geeksforgeeks.org/python-sympy-mul-method/)

借助`**sympy.Mul()**`方法，我们可以将两个变量相乘，并可以形成一个数学表达式。

> **语法:** `sympy.Mul()`
> **返回:**返回两个变量的乘积。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.Mul()`方法，我们能够将两个变量相乘，并且我们还可以形成数学表达式。

```py
# import sympy
from sympy import * x, y = symbols('x y')

# Use sympy.Mul() method
mul = Mul(x, y)

print(mul)
```

**输出:**

> x*y

**例 2 :**

```py
# import sympy
from sympy import * x, y = symbols('x y')

# Use sympy.Mul() method
 mul = Mul(x, y) + Mul(x, x)

print(mul)
```

**输出:**

> x**2 + x*y
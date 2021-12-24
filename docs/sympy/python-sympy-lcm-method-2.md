# Python | sympy.lcm()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-lcm-method-2/](https://www.geeksforgeeks.org/python-sympy-lcm-method-2/)

The function `lcm()` provides the direct way to compute Least Common Multiple for polynomials.That is, for polynomials f and g, it computes LCM.

```
Syntax: sympy.lcm(f, g)

Return: LCM of given polynomials

```

示例#1:

```
# import sympy  
from sympy import * f = x * y**2 + x**2 * y
g = x**2 * y**2

# Using sympy.lcm() method 
gfg = lcm(f, g)

print(gfg)
```

**输出:**

```
x**3*y**2 + x**2*y**3

```

示例 2:

```
# import sympy  
from sympy import * f = x * y / 2 + y**2
g = 3 * x + 6 * y

# Using sympy.lcm() method 
gfg = lcm(f, g)

print(gfg)
```

**输出:**

```
x*y + 2*y**2

```
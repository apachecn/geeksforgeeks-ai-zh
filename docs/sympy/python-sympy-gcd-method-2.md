# Python | sympy.gcd()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-gcd-method-2/](https://www.geeksforgeeks.org/python-sympy-gcd-method-2/)

函数`gcd()`提供了计算多项式最大公约数的直接方法。也就是说，对于多项式 f 和 g，它计算 GCD。

```
Syntax: sympy.gcd(f, g)

Return: GCD of given polynomials

```

**例#1:**

```
# import sympy  
from sympy import * f = (12 * x + 12)*x
g = 32 * x**2

# Using sympy.gcd() method 
gfg = gcd(f, g)  

print(gfg)
```

**输出:**

```
4*x
```

**例#2:**

```
# import sympy  
from sympy import * f = 3 * x**2 / 2
g = 9 * x / 4

# Using sympy.gcd() method 
gfg = gcd(f, g)  

print(gfg)
```

**输出:**

```
x
```
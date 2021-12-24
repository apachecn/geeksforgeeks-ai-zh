# Python | sympy.div()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-div-method/](https://www.geeksforgeeks.org/python-sympy-div-method/)

The function `div()` provides division of polynomials with remainder. That is, for polynomials f and g, it computes q and r, such that **`f= g*q+r`** and `deg(r) <q.`

```
Syntax:sympy.div(f, g, domain='QQ')
Return: division of polynomials with remainder

```

**示例#1:**

```
# import sympy 
from sympy import * 

f = 5 * x**2 + 10 * x + 3
g = 2 * x + 2

# Using sympy.div() method 
q, r = div(f, g, domain ='QQ')

print(q)
print(r)
```

**输出:**

```
5*x/2 + 5/2
-2

```

**示例#2:**

```
# import sympy 
from sympy import * 

f = 5 * x**2 + 10 * x + 3
g = 2 * x**2 + 2

# Using sympy.div() method 
q, r = div(f, g, domain ='QQ')

print(q)
print(r)
```

**输出:**

```
5/2
10*x - 2

```
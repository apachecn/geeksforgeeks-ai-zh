# Python 中的 sympy.stats .多项式()函数

> 原文:[https://www . geesforgeks . org/sympy-stats-多项式-python 中的函数/](https://www.geeksforgeeks.org/sympy-stats-multinomial-function-in-python/)

借助**方法，我们可以创建一个具有多项式分布的离散随机变量。**

多项式分布是多项式实验结果的概率分布。

```
Syntax: sympy.stats.Multinomial(syms, n, p)

Parameters: 
 syms: the symbol
 n: is the number of trials, a positive integer
 p: event probabilites, p>= 0 and p<= 1

Returns: a discrete random variable with Multinomial Distribution

```

**示例#1 :**

## 蟒蛇 3

```
# import sympy, Multinomial, density, symbols
from sympy.stats.joint_rv_types import Multinomial
from sympy.stats import density
from sympy import symbols, pprint

x1, x2, x3 = symbols('x1, x2, x3', nonnegative = True, integer = True)
p1, p2, p3 = symbols('p1, p2, p3', positive = True)

# Using sympy.stats.Multinomial() method
M = Multinomial('M', 3, p1, p2, p3)
multiDist = density(M)(x1, x2, x3)

pprint(multiDist)
```

**输出:**

```
/    x1   x2   x3                      
|6*p1  *p2  *p3                        
|----------------  for x1 + x2 + x3 = 3
<  x1!*x2!*x3!                         
|                                      
|       0               otherwise      
\                                   

```

**例 2 :**

## 蟒蛇 3

```
# import sympy, Multinomial, density, symbols
from sympy.stats.joint_rv_types import Multinomial
from sympy.stats import density
from sympy import symbols, pprint

x1, x2, x3 = symbols('x1, x2, x3', nonnegative = True, integer = True)

# Using sympy.stats.Multinomial() method
M = Multinomial('M', 4, 0, 1, 0)
multiDist = density(M)(x1, x2, x3)

pprint(multiDist)
```

**输出:**

```
/     x1  x3                      
| 24*0  *0                        
|-----------  for x1 + x2 + x3 = 4
<x1!*x2!*x3!                      
|                                 
|     0            otherwise      
\                                

```
# Python | sympy.multiplicity()方法

> 原文:[https://www . geesforgeks . org/python-sympy-multiplicity-method/](https://www.geeksforgeeks.org/python-sympy-multiplicity-method/)

借助 **sympy.multiplicity()** 方法，我们可以找到最大的整数 ***m*** 这样 ***p*** 上升到*T11】mT13】除*T15】nT17】，其中**T19】p***T21*T23】nT25】是该方法的参数**

> **语法:**
> 多重性(p，n)
> 
> **参数:**
> **p–**表示整数。
> **n–**表示整数。
> 
> **返回:**
> 返回最大整数 m，使得 p^m 除 n。

**示例#1:**

```
# import multiplicity() method from sympy
from sympy import multiplicity

p = 2
n = 64

# Use multiplicity() method 
multi_p_n = multiplicity(p, n) 

print("{} is the largest integer such that {}^{} divides {}.".
      format(multi_p_n, p, multi_p_n, n))
```

**输出:**

```
6 is the largest integer such that 2^6 divides 64.

```

**例 2:**

```
# import multiplicity() method from sympy
from sympy import multiplicity

p = 3
n = 111

# Use multiplicity() method 
multi_p_n = multiplicity(p, n) 

print("{} is the largest integer such that {}^{} divides {}.".
      format(multi_p_n, p, multi_p_n, n))
```

**输出:**

```
1 is the largest integer such that 3^1 divides 111.

```
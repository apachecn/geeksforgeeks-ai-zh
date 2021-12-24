# Python | sympy.primefactors()方法

> 原文:[https://www . geesforgeks . org/python-sympy-prime factors-method/](https://www.geeksforgeeks.org/python-sympy-primefactors-method/)

借助 **sympy.primefactors()** 方法，可以求出给定数的素数因子。与**factory int()**不同， **primefactors()** 不返回 *-1* 或 *0* 。

> **语法:**素因子(n)
> 
> **参数:**
> **n–**表示整数。
> 
> **返回:**返回给定整数的质因数列表。

**示例#1:**

```
# import primefactors() method from sympy
from sympy import primefactors

n = 2 * 6*21 * 11

# Use primefactors() method 
primefactors_n = primefactors(n) 

print("The prime factors of {} : {}".format(n, primefactors_n))
```

**输出:**

```
The prime factors of 2772 : [2, 3, 7, 11]

```

**例 2:**

```
# import primefactors() method from sympy
from sympy import primefactors

n = -210

# Use primefactors() method 
primefactors_n = primefactors(n) 

print("The prime factors of {} : {}".format(n, primefactors_n))
```

**输出:**

```
The prime factors of -210 : [2, 3, 5, 7]

```
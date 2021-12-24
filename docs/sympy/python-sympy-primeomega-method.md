# Python | sympy.primeomega()方法

> 原文:[https://www . geesforgeks . org/python-sympy-prime omega-method/](https://www.geeksforgeeks.org/python-sympy-primeomega-method/)

借助 **sympy.primeomega()** 方法，我们可以计算出给定正整数的计算重数的素因子个数。例如 *primeomega(12) = 3* ，因为*12 = 2<sup>2</sup>* 3<sup>1</sup>T9】。因此，素因子数=素因子的倍数之和， *2 + 1 = 3。**

> **语法:**素数(n)
> 
> **参数:**
> **n–**表示整数。
> 
> **返回:**返回给定正整数的重数素数。

**示例#1:**

```
# import primeomega() method from sympy
from sympy.ntheory.factor_ import primeomega

n = 24

# Use primeomega() method 
primeomega_n = primeomega(n) 

print(" Number of prime factors of {} = {} ".format(n, primeomega_n))
```

**输出:**

```
Number of prime factors of 24 = 4 

```

**例 2:**

```
# import primeomega() method from sympy
from sympy.ntheory.factor_ import primeomega

n = 120

# Use primeomega() method 
primeomega_n = primeomega(n) 

print(" Number of prime factors of {} = {} ".format(n, primeomega_n))
```

**输出:**

```
Number of prime factors of 120 = 5 

```
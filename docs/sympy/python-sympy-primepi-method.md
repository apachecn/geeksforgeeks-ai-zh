# Python | sympy . primpi()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-primepi-method/](https://www.geeksforgeeks.org/python-sympy-primepi-method/)

借助 **sympy.primepi()** 方法，我们可以求出小于等于给定数的素数个数。

> **语法:** primepi(n)
> 
> **参数:**
> **n–**表示计算素数个数的个数。
> 
> **返回:**返回小于或等于 **n** 的素数。

**示例#1:**

```py
# import primepi() method from sympy
from sympy import primepi

n = 10

# Use primepi() method 
count_primes = primepi(n) 

print("The number of prime numbers less than or equal to {} is {}".format(n, count_primes))
```

**输出:**

```py
The number of prime numbers less than or equal to 10 is 4

```

**例 2:**

```py
# import primepi() method from sympy
from sympy import primepi

n = 150

# Use primepi() method 
count_primes = primepi(n) 

print("The number of prime numbers less than or equal to {} is {}".format(n, count_primes))          
```

**输出:**

```py
The number of prime numbers less than or equal to 150 is 35

```
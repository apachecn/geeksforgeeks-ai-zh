# Python | symy . primorial()方法

> 原文:[https://www . geesforgeks . org/python-sympy-primorial-method/](https://www.geeksforgeeks.org/python-sympy-primorial-method/)

借助 **sympy.primorial()** 方法，我们可以找到第一个 ***n*** 素数(默认)或小于或等于 ***n*** 的素数(当***n = False***时)的乘积，其中 ***n*** 和***n***是该方法的参数。

> **语法:**primary(n，n)
> 
> **参数:**
> **n–**表示计算前 n 个素数或小于等于 n 的素数的乘积的个数。
> **第 n–**表示布尔值。当为真时，它返回前 n 个素数的乘积，而当为假时，它返回小于或等于 n 的素数的乘积
> 
> **返回:**返回前 n 个素数或小于等于 n 的素数的乘积。

**示例#1:**

```
# import primorial() method from sympy
from sympy import primorial

n = 3

# Use primorial() method 
primorial_n = primorial(n) # 2 * 3 * 5

print("The product of first {} primes is {}".format(n, primorial_n))
```

**输出:**

```
The product of first 3 primes is 30

```

**例 2:**

```
# import primorial() method from sympy
from sympy import primorial

n = 10

# Use primorial() method 
primorial_n = primorial(n, nth = False) # 2 * 3 * 5 * 7

print("The product of primes less than or equal to {} is {}".format(n, primorial_n))          
```

**输出:**

```
The product of primes less than or equal to 10 is 210

```
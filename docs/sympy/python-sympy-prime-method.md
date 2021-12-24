# Python | sympy.prime()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-prime-method/](https://www.geeksforgeeks.org/python-sympy-prime-method/)

借助 **sympy.prime()** 方法，可以找到*第 n 个*素数，素数索引为*素数(1) = 2，素数(2) = 3* 等。

> **语法:**质数(n)
> 
> **参数:**
> **n–**表示第 n 个素数。
> 
> **返回:**返回第 n 个素数。

**示例#1:**

```
# import sympy 
from sympy import prime

n = 5

# Use prime() method 
nth_prime = prime(n) 

print("The {}th prime is {}".format(n, nth_prime))  
```

**输出:**

```
The 5th prime is 11

```

**例 2:**

```
# import sympy 
from sympy import prime

n = 23

# Use prime() method 
nth_prime = prime(n) 

print("The {}rd prime is {}".format(n, nth_prime))        
```

**输出:**

```
The 23rd prime is 83

```
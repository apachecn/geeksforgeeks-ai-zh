# Python | sympy.primenu()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-primenu-method/](https://www.geeksforgeeks.org/python-sympy-primenu-method/)

借助 **sympy.primenu()** 方法，我们可以计算给定正整数的不同素数因子的个数。

> **语法:**素数(n)
> 
> **参数:**
> **n–**表示整数。
> 
> **返回:**返回给定正整数的不同质因数的个数。

**示例#1:**

```
# import primenu() method from sympy
from sympy.ntheory.factor_ import primenu

n = 24

# Use primenu() method 
primenu_n = primenu(n) 

print("Number of distinct prime factors of {} = {} ".format(n, primenu_n)) # 2 and 3
```

**输出:**

```
Number of distinct prime factors of 24 = 2  

```

**例 2:**

```
# import primenu() method from sympy
from sympy.ntheory.factor_ import primenu

n = 2 * 3*7 * 11 * 13

# Use primenu() method 
primenu_n = primenu(n) 

print("Number of distinct prime factors of {} = {} ".format(n, primenu_n))  
```

**输出:**

```
Number of distinct prime factors of 6006 = 5 

```
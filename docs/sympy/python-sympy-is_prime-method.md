# Python | sympy.is_prime()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-is_prime-method/](https://www.geeksforgeeks.org/python-sympy-is_prime-method/)

在 simpy 模块中，我们可以使用 sympy.is_prime()函数来测试给定的数字 n 是否是素数。对于 n < 2^64，答案是确定的；较大的 n 值实际上是伪素数的概率很小。

请注意，负数(例如-13)不被视为质数。

```py
Syntax:  sympy.is_prime()
Parameter:  n; number to be tested
Return:  bool value result 
```

**代码#1:**

## 蟒蛇 3

```py
# Python program to check prime number
# using sympy.is_prime() method

# importing sympy module
from sympy import *

# calling isprime function on different numbers
geek1 = simplify(30).is_prime
geek2 = simplify(13).is_prime

print(geek1)
print(geek2)
```

输出:

```py
False
True
```

**代码#2:**

## 蟒蛇 3

```py
# Python program to check prime number
# using sympy.is_prime() method

# importing sympy module
from sympy import *

# calling isprime function on different numbers
geek = simplify(2).is_prime

print(geek)
```

输出:

```py
True
```
# Python | sympy.isprime()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-isprime-method/](https://www.geeksforgeeks.org/python-sympy-isprime-method/)

在 simpy 模块中，我们可以使用 sympy.isprime()函数来测试给定的数字 n 是否是素数。对于 n < 2^64，答案是确定的；较大的 n 值实际上是伪素数的概率很小。

请注意，负数(例如-13)不被视为质数。

```py
Syntax:  sympy.isprime()
Parameter:  n; number to be tested
Return:  bool value result 
```

**代码#1:**

## 蟒蛇 3

```py
# Python program to check prime number
# using sympy.isprime() method

# importing sympy module
from sympy import *

# calling isprime function on different numbers
isprime(30)
isprime(13)
isprime(2)
```

输出:

```py
False
True
True
```

**代码#2:**

## 蟒蛇 3

```py
# Python program to check prime number
# using sympy.isprime() method

# importing sympy module
import sympy.ntheory as nt

# calling isprime function on different numbers
nt.isprime(30)
nt.isprime(13)
nt.isprime(2)
```

输出:

```py
False
True
True
```
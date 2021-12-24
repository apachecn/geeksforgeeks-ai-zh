# Python | sympy.is_odd()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-is_odd-method/](https://www.geeksforgeeks.org/python-sympy-is_odd-method/)

在 simpy 模块中，我们可以使用 `sympy.is_odd()`函数测试给定的数字 n 是否为奇数。

```py
Syntax:  sympy.is_odd(n)
Parameter:  n; number to be tested
Return:  bool value result 

```

**代码#1:**

```py
# Python program to check odd number
# using sympy.is_odd() method

# importing sympy module
from sympy import *

# calling is_odd function on different numbers
geek1 = simplify(30).is_odd
geek2 = simplify(13).is_odd

print(geek1)
print(geek2)
```

输出:

```py
False
True

```

**代码#2:**

```py
# Python program to check odd number
# using sympy.is_odd() method

# importing sympy module
from sympy import *

# calling is_odd function on different numbers
geek = simplify(2).is_odd

print(geek)
```

输出:

```py
False
```
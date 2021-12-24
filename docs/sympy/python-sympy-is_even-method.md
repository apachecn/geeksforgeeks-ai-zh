# Python | sympy.is_even()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-is_even-method/](https://www.geeksforgeeks.org/python-sympy-is_even-method/)

在 simpy 模块中，我们可以使用 sympy.is_even()函数来测试给定的数字 n 是否为偶数。

```
Syntax:  sympy.is_even(n)
Parameter:  n; number to be tested
Return:  bool value result 
```

**代码#1:**

## 蟒蛇 3

```
# Python program to check even number
# using sympy.is_even() method

# importing sympy module
from sympy import *

# calling is_evenfunction on different numbers
geek1 = simplify(30).is_even
geek2 = simplify(13).is_even

print(geek1)
print(geek2)
```

输出:

```
True
False
```

**代码#2:**

## 蟒蛇 3

```
# Python program to check even number
# using sympy.is_even() method

# importing sympy module
from sympy import *

# calling is_even function on different numbers
geek = simplify(2).is_even

print(geek)
```

输出:

```
True
```
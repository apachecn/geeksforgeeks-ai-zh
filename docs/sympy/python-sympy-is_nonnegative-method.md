# Python | sympy.is_nonnegative()方法

> 原文:[https://www . geesforgeks . org/python-sympy-is _ nonnegative-method/](https://www.geeksforgeeks.org/python-sympy-is_nonnegative-method/)

在 simpy 模块中，我们可以使用 sympy.is_nonnegative()函数来测试给定的数字 n 是否为非负。

```py
Syntax:  sympy.is_nonnegative(n)
Parameter:  n; number to be tested
Return:  bool value result 
```

**代码#1:**

## 蟒蛇 3

```py
# Python program to check nonnegative number
# using sympy.is_nonnegative() method

# importing sympy module
from sympy import *

# calling is_nonnegative function on different numbers
geek1 = simplify(-21).is_nonnegative
geek2 = simplify(0).is_nonnegative

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
# Python program to check nonnegative number
# using sympy.is_nonnegative() method

# importing sympy module
from sympy import *

# calling is_negative function on different numbers
geek = simplify(-002).is_nonnegative

print(geek)
```

输出:

```py
False
```
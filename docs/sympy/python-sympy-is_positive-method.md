# Python | sympy.is_positive()方法

> 原文:[https://www . geesforgeks . org/python-sympy-is _ positive-method/](https://www.geeksforgeeks.org/python-sympy-is_positive-method/)

在 simpy 模块中，我们可以使用 sympy.is_positive()函数来测试给定的数字 n 是否为正。

```
Syntax:  sympy.is_positive(n)
Parameter:  n; number to be tested
Return:  bool value result 
```

**代码#1:**

## 蟒蛇 3

```
# Python program to check positive number
# using sympy.is_positive() method

# importing sympy module
from sympy import *

# calling is_positive function on different numbers
geek1 = simplify(-21).is_positive
geek2 = simplify(0).is_positive

print(geek1)
print(geek2)
```

输出:

```
False
True
```

**代码#2:**

## 蟒蛇 3

```
# Python program to check positive  number
# using sympy.is_positive() method

# importing sympy module
from sympy import *

# calling is_positive function on different numbers
geek = simplify(-002).is_positive

print(geek)
```

输出:

```
False
```
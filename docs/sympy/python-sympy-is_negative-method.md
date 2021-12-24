# Python | sympy.is_negative()方法

> 原文:[https://www . geesforgeks . org/python-sympy-is _ negative-method/](https://www.geeksforgeeks.org/python-sympy-is_negative-method/)

在 simpy 模块中，我们可以使用 sympy.is_negative()函数来测试给定的数字 n 是否为负。

```
Syntax:  sympy.is_negative(n)
Parameter:  n; number to be tested
Return:  bool value result 
```

**代码#1:**

## 蟒蛇 3

```
# Python program to check negative number
# using sympy.is_negative() method

# importing sympy module
from sympy import *

# calling is_negative function on different numbers
geek1 = simplify(-21).is_negative
geek2 = simplify(0).is_negative

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
# Python program to check negative number
# using sympy.is_negative() method

# importing sympy module
from sympy import *

# calling is_negative function on different numbers
geek = simplify(-002).is_negative

print(geek)
```

输出:

```
True
```
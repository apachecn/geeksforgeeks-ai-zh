# Python | sympy . is _ 非零()方法

> 原文:[https://www . geesforgeks . org/python-sympy-is _ 非零-method/](https://www.geeksforgeeks.org/python-sympy-is_nonzero-method/)

在 simpy 模块中，我们可以使用 sympy.is _ 非零()函数来测试给定的数字 n 是否非零。

```
Syntax:  sympy.is_nonzero(n)
Parameter:  n; number to be tested
Return:  bool value result 
```

**代码#1:**

## 蟒蛇 3

```
# Python program to check nonzero
# using sympy.is_nonzero() method

# importing sympy module
from sympy import *

# calling is_nonzero function on different numbers
geek1 = simplify(21).is_nonzero
geek2 = simplify(0).is_nonzero

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
# Python program to check nonzero number
# using sympy.is_nonzero() method

# importing sympy module
from sympy import *

# calling is_nonzero function on different numbers
geek = simplify(002).is_nonzero

print(geek)
```

输出:

```
True
```
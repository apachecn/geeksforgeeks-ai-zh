# Python | sympy.is_nonpositive()方法

> 原文:[https://www . geesforgeks . org/python-sympy-is _ nonpositive-method/](https://www.geeksforgeeks.org/python-sympy-is_nonpositive-method/)

在 simpy 模块中，我们可以使用 sympy.is_nonpositive()函数

```
Syntax:  sympy.is_nonpositive(n)
Parameter:  n; number to be tested
Return:  bool value result 
```

来测试给定的数字 n 是否为非正

**代码#1:**

## 蟒蛇 3

```
# Python program to check non-positive number
# using sympy.is_nonpositive() method

# importing sympy module
from sympy import *

# calling is_nonpositive function on different numbers
geek1 = simplify(-21).is_nonpositive
geek2 = simplify(0).is_nonpositive

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
# Python program to check non-positive number
# using sympy.is_nonpositive() method

# importing sympy module
from sympy import *

# calling is_nonpositive function on different numbers
geek = simplify(-002).is_nonpositive

print(geek)
```

输出:

```
True
```
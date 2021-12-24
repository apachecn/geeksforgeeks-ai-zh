# Python | sympy.is_zero()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-is_zero-method/](https://www.geeksforgeeks.org/python-sympy-is_zero-method/)

在 simpy 模块中，我们可以使用 sympy.is_zero()函数来测试给定的数字 n 是否为零。

```
Syntax:  sympy.is_zero(n)
Parameter:  n; number to be tested
Return:  bool value result 
```

**代码#1:**

## 蟒蛇 3

```
# Python program to check zero
# using sympy.is_zero() method

# importing sympy module
from sympy import *

# calling is_zero function on different numbers
geek1 = simplify(1).is_zero
geek2 = simplify(0).is_zero

print(geek1)
print(geek2)
```

**输出:**

```
False
True
```

**代码#2:**

## 蟒蛇 3

```
# Python program to check zero number
# using sympy.is_zero() method

# importing sympy module
from sympy import *

# calling is_zero function on different numbers
geek = simplify(002).is_zero

print(geek)
```

**输出:**

```
False
```
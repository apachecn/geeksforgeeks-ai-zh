# Python | sympy is _ 共线()方法

> 原文:[https://www . geesforgeks . org/python-sympy-is _ 共线-method/](https://www.geeksforgeeks.org/python-sympy-is_collinear-method/)

函数 is _ collinear()使我们能够检查给定点(坐标)是否共线
。

```
Syntax: 

Parameters:  x, y, z are coordinates.

Return: True : if points are collinear, otherwise False.
```

**示例#1:**

## 蟒蛇 3

```
# import sympy and geometry module
from sympy import *
from sympy.geometry import *

x = Point(0, 0)
y = Point(1, 1)
z = Point(2, 2)

# Using Point.is_collinear() method
isTrue = Point.is_collinear(x, y, z)

print(isTrue)
```

**输出:**

```
True
```

**例 2:**

## 蟒蛇 3

```
# import sympy and geometry module
from sympy import *
from sympy.geometry import *

x = Point(1, 0)
y = Point(1, 2)
z = Point(2, 2)

# Using Point.is_collinear() method
isTrue = Point.is_collinear(x, y, z)

print(isTrue)
```

**输出:**

```
False
```
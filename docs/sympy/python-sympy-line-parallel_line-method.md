# Python | Sympy line . parallel _ line 方法

> 原文:[https://www . geesforgeks . org/python-sympy-line-parallel _ line-method/](https://www.geeksforgeeks.org/python-sympy-line-parallel_line-method/)

在 Sympy 中，函数 parallel_line()用于创建一条平行于给定线性实体的新直线，该直线穿过给定点 p.

```py
Syntax: Line.parallel_line(p)

Parameters:
p: Point

Returns: Line
```

**示例#1:**

## 蟒蛇 3

```py
# import sympy and Point, Line
from sympy import Point, Line

p1, p2, p3 = Point(0, 0), Point(2, 3), Point(-2, 2)

l1 = Line(p1, p2)

# using parallel_line() method
l2 = l1.parallel_line(p3)

# checking l2 is parallel to l1 using is_parallel() method
isParallel = l1.is_parallel(l2)

print(isParallel)
```

**输出:**

```py
True
```

**例 2:**

## 蟒蛇 3

```py
# import sympy and Point3D, Line3D
from sympy import Point3D, Line3D

p1, p2, p3 = Point3D(0, 0, 0), Point3D(2, 3, 4), Point3D(-2, 2, 0)

l1 = Line3D(p1, p2)

# using parallel_line() method
l2 = l1.parallel_line(p3)

# checking l2 is parallel to l1 using is_parallel() method
isParallel = l2 = l1.is_parallel(p3)

print(isParallel)
```

**输出:**

```py
True 
```
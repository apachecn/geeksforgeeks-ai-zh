# Python–Sympy . triangle . is _ scalene()方法

> 原文:[https://www . geesforgeks . org/python-sympy-triangle-is _ scalene-method/](https://www.geeksforgeeks.org/python-sympy-triangle-is_scalene-method/)

In Sympy, the function `Triangle.is_scalene()` is used to check whether the given triangle is Scalene Triangle or not. Scalene Triangle is the triangle in which all the sides are of different lengths.

```
Syntax: Triangle.is_scalene()

Returns: 
 True: if it is scalene, otherwise False

```

**示例#1:**

```
# import Triangle, Point
from sympy.geometry import Triangle, Point

# using Triangle()
t1 = Triangle(Point(0, 0), Point(3, 0), Point(1, 2))

# using is_scalene()
isScalene = t1.is_scalene()
print(isScalene)
```

**输出:**

```
True
```

**示例#2:**

```
# import Triangle, Point
from sympy.geometry import Triangle, Point

# using Triangle()
t2 = Triangle(Point(0, 0), Point(4, 0), Point(2, 4))

# using is_scalene()
isScalene = t2.is_scalene()
print(isScalene)
```

**输出:**

```
False
```
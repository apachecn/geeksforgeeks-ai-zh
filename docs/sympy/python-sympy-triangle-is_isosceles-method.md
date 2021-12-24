# Python–Sympy triangle . is _ 等腰()方法

> 原文:[https://www . geesforgeks . org/python-sympy-triangle-is _ 等腰-method/](https://www.geeksforgeeks.org/python-sympy-triangle-is_isosceles-method/)

In Sympy, the function Triangle.is_isosceles() is used to check whether the given triangle is Isosceles triangle or not. Isosceles Triangle is the triangle in which two or more of the sides are of the same length.

```
Syntax: Triangle.is_isosceles()

Returns: 
 True: if it is isosceles, otherwise False

```

**示例#1:**

```
# import Triangle, Point
from sympy.geometry import Triangle, Point

# using Triangle()
t1 = Triangle(Point(0, 0), Point(6, 0), Point(3, 4))

# using is_isosceles()
isIsosceles = t1.is_isosceles()
print(isIsosceles)
```

输出:

```
True
```

**示例#2:**

```
# import Triangle, Point
from sympy.geometry import Triangle, Point

# using Triangle()
t2 = Triangle(Point(0, 0), Point(3, 0), Point(3, 4))

# using is_isosceles()
isIsosceles = t2.is_isosceles()
print(isIsosceles)
```

输出:

```
False
```
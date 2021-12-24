# Python–Sympy triangle . is _ right()方法

> 原文:[https://www . geesforgeks . org/python-sympy-triangle-is _ right-method/](https://www.geeksforgeeks.org/python-sympy-triangle-is_right-method/)

In Sympy, the function `Triangle.is_right()` is used to check whether the given triangle is Right-Angled Triangle or not. Right-Angled Triangle is the triangle in which one angle is a right angle(90 degrees).

```
Syntax: Triangle.is_right()

Returns: 
 True: if it is right-angled, otherwise False

```

**示例#1:**

```
# import Triangle, Point
from sympy.geometry import Triangle, Point

# using Triangle()
t1 = Triangle(Point(0, 0), Point(4, 0), Point(4, 3))

# using is_right()
isRight = t1.is_right()
print(isRight)
```

**输出:**

```
True
```

**例 2:**

```
# import Triangle, Point
from sympy.geometry import Triangle, Point

# using Triangle()
t2 = Triangle(Point(0, 0), Point(2, 0), Point(4, 3))

# using is_right()
isRight = t2.is_right()
print(isRight)
```

**输出:**

```
False
```
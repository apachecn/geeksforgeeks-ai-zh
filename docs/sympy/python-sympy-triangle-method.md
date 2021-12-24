# Python | symy Triangle()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-triangle-method/](https://www.geeksforgeeks.org/python-sympy-triangle-method/)

The function `Trianlgle()` takes the given points as vertices of a triangle and computes the area of triangle with the help of area.

```
Syntax: Triangle(x, y, z).area

Parameters: where x, y, z are coordinates.

Return: Area of triangle.

```

**示例#1:**

```
# import sympy and geometry module
from sympy import * 
from sympy.geometry import * 

x = Point(0, 0)
y = Point(1, 1)
z = Point(1, 0)

# Using  Triangle(x, y, z).area
giveArea = Triangle(x, y, z).area

print(giveArea)
```

**输出:**

```
1/2
```

**例 2:**

```
# import sympy and geometry module
from sympy import * 
from sympy.geometry import * 

x = Point(1, 2)
y = Point(2, 0)
z = Point(1, 0)

# Using  Triangle(x, y, z).area
giveArea = Triangle(x, y, z).area

print(giveArea)
```

**输出:**

```
1
```
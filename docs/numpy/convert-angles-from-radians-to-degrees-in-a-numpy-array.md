# 在 NumPy 数组中将角度从弧度转换为度数

> 原文:[https://www . geeksforgeeks . org/convert-angles-从弧度到角度-in-numpy-array/](https://www.geeksforgeeks.org/convert-angles-from-radians-to-degrees-in-a-numpy-array/)

在本文中，我们将讨论如何将由不同角度组成的数组元素从弧度转换为度数。

要将角度从弧度转换为度数，我们只需将弧度乘以 180/π？。我们也可以使用 [numpy.rad2deg()](https://www.geeksforgeeks.org/numpy-degrees-rad2deg-python/) 方法进行同样的操作。

现在假设我们有一个包含弧度角度的数组，现在我们的任务是将该数组转换为包含度数元素的元素。
**例:**

```py
Input : [Π, Π/4, Π/2, 3Π/2, 2Π)
Output : [180\.  45\.  90\. 270\. 360.]

```

现在让我们尝试使用 Python 来实现这一点:

**示例 1 :** 我们将使用π的 **numpy.pi** 属性。

```py
# importing the module
import numpy as np

# creating an array containing angles in radians
rad = np.array([np.pi, np.pi / 4,
                np.pi / 2, 3 * np.pi / 2,
                2 * np.pi])
print("The angles in radian")
print(rad)

# converting array from radian to degree
deg = np.rad2deg(rad)
print("\nThe angles in degree")
print(deg)
```

**输出:**

```py
The angles in radian
[3.14159265 0.78539816 1.57079633 4.71238898 6.28318531]

The angles in degree
[180\.  45\.  90\. 270\. 360.]

```

**示例 2 :** 这一次将在不使用内置方法的情况下执行转换。

```py
# importing the module
import numpy as np

# creating an array containing angles in radians
rad = np.array([3.14159265, 0.78539816,
                1.57079633, 4.71238898,
                6.28318531])
print("The angles in radian")
print(rad)

# converting array from radian to degree
deg = []
for angle in rad:
    deg.append(round(angle * (180 / np.pi)))
print("\nThe angles in degree")
print(deg)
```

**输出:**

```py
The angles in radian
[3.14159265 0.78539816 1.57079633 4.71238898 6.28318531]

The angles in degree
[180.0, 45.0, 90.0, 270.0, 360.0]

```
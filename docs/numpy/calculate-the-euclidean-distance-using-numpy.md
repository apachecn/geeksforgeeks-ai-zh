# 使用 NumPy

计算欧氏距离

> 原文:[https://www . geeksforgeeks . org/compute-the-euclidean-distance-use-numpy/](https://www.geeksforgeeks.org/calculate-the-euclidean-distance-using-numpy/)

简单来说，欧几里得距离是两点之间最短的，与维度无关。在本文中要找到欧几里得距离，我们将使用 [NumPy](https://www.geeksforgeeks.org/python-numpy/) 库。这个库用于以非常有效的方式操作多维数组。我们来讨论几个利用 NumPy 库求欧氏距离的方法。

**方法#1:使用 linalg . norm()**

## python 3

```
# Python code to find Euclidean distance
# using linalg.norm()

import numpy as np

# initializing points in
# numpy arrays
point1 = np.array((1, 2, 3))
point2 = np.array((1, 1, 1))

# calculating Euclidean distance
# using linalg.norm()
dist = np.linalg.norm(point1 - point2)

# printing Euclidean distance
print(dist)
```
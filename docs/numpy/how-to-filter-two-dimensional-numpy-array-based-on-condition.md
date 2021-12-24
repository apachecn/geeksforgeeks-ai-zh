# 如何基于条件过滤二维 NumPy 数组？

> 原文:[https://www . geeksforgeeks . org/如何过滤-二维-numpy-数组-基于条件/](https://www.geeksforgeeks.org/how-to-filter-two-dimensional-numpy-array-based-on-condition/)

在本文中，我们将看到如何在 NumPy 二维数组中应用给定条件的过滤器。我们必须获得所需元素的输出，即我们想要从现有数组或新数组中过滤的元素。

**这里我们要在 numpy 中创建一个二维数组。**

## 蟒 3

```
import numpy as np

# 2-D Array also called as arrays 
# with rank 2
np_2d_arr = np.array([[1, 2, 3], [4, 5, 6]])

# View the 2-D Array A2
print(np_2d_arr)
```
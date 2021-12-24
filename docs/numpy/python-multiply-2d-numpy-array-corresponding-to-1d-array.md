# Python |乘以 1d 数组对应的 2d numpy 数组

> 原文:[https://www . geesforgeks . org/python-multiply-2d-numpy-array-对应-1d-array/](https://www.geeksforgeeks.org/python-multiply-2d-numpy-array-corresponding-to-1d-array/)

给定两个 numpy 数组，任务是将 2d numpy 数组乘以 1d numpy 数组，每行对应 numpy 中的一个元素。让我们讨论给定任务的几种方法。

**方法#1:使用 np.newaxis()**

```
# Python code to demonstrate
# multiplication of 2d array
# with 1d array

import numpy as np

ini_array1 = np.array([[1, 2, 3], [2, 4, 5], [1, 2, 3]])
ini_array2 = np.array([0, 2, 3])

# printing initial arrays
print("initial array", str(ini_array1))

# Multiplying arrays
result = ini_array1 * ini_array2[:, np.newaxis]

# printing result
print("New resulting array: ", result)
```

**输出:**

```
initial array [[1 2 3]
 [2 4 5]
 [1 2 3]]
New resulting array:  [[ 0  0  0]
 [ 4  8 10]
 [ 3  6  9]]

```
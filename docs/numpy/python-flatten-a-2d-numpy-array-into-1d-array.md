# Python |将 2d numpy 数组展平为 1d 数组

> 原文:[https://www . geesforgeks . org/python-flat-a-2d-numpy-array-in-1d-array/](https://www.geeksforgeeks.org/python-flatten-a-2d-numpy-array-into-1d-array/)

给定 2d numpy 数组，任务是将 2d numpy 数组展平为 1d 数组。下面是几个解决任务的方法。

**方法#1:使用 NP . flat()**

```py
# Python code to demonstrate
# flattening a 2d numpy array
# into 1d array

import numpy as np

ini_array1 = np.array([[1, 2, 3], [2, 4, 5], [1, 2, 3]])

# printing initial arrays
print("initial array", str(ini_array1))

# Multiplying arrays
result = ini_array1.flatten()

# printing result
print("New resulting array: ", result)
```

**输出:**

```py
initial array [[1 2 3]
 [2 4 5]
 [1 2 3]]
New resulting array:  [1 2 3 2 4 5 1 2 3]

```
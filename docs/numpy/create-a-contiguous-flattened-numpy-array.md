# 创建一个连续的扁平 NumPy 数组

> 原文:[https://www . geeksforgeeks . org/create-a-contact-flated-numpy-array/](https://www.geeksforgeeks.org/create-a-contiguous-flattened-numpy-array/)

让我们看看如何在 NumPy 中创建一个连续的数组。连续的扁平数组是二维和多维数组，存储为一维数组。我们将使用 [ravel()](https://www.geeksforgeeks.org/numpy-ravel-python/) 方法来执行此任务。

> **语法:** numpy.ravel(数组，顺序= 'C')
> **参数:**
> 
> *   **数组:**输入数组。
> *   **顺序:** C 连片、F 连片、A 连片；可选择的
> 
> **返回:**扁平数组，其类型与输入数组相同，并根据选择进行排序。

**例 1 :** 展平 2D 阵。

## 蟒蛇 3

```py
# Importing libraries
import numpy as np

# Creating 2D array
arr = np.array([[5, 6, 7], [8, 9, 10]])
print("Original array:\n", arr)

# Flattening the array
flattened_array = np.ravel(arr)
print("New flattened array:\n", flattened_array)
```

**输出:**

```py
Original array:
 [[ 5  6  7]
 [ 8  9 10]]
New flattened array:
 [ 5  6  7  8  9 10]

```

**示例 2 :** 展平三维阵列。

## 蟒蛇 3

```py
# Importing libraries
import numpy as np

# Creating 3D array
arr = np.array([[[3, 4], [5, 6]], [[7, 8], [9, 0]]])
print("Original array:\n", arr)

# Flattening the array
flattened_array = np.ravel(arr)
print("New flattened array:\n", flattened_array)
```

**输出:**

```py
Original array:
 [[[3 4]
  [5 6]]

 [[7 8]
  [9 0]]]
New flattened array:
 [3 4 5 6 7 8 9 0]

```
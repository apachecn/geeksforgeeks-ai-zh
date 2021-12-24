# 计算两个给定 NumPy 阵列的平均值

> 原文:[https://www . geeksforgeeks . org/计算两个给定 numpy 数组的平均值/](https://www.geeksforgeeks.org/calculate-average-values-of-two-given-numpy-arrays/)

求 NumPy 数组的平均值与求给定数字的平均值非常相似。我们只需要得到相应数组元素的和，然后用这个和除以数组的总数。

让我们看一个例子:

**示例 1:** 计算两个给定 NumPy 1d 阵列的平均值

## 蟒蛇 3

```py
# import library
import numpy as np

#  create a numpy 1d-arrays
arr1 = np.array([3, 4])
arr2 = np.array([1, 0])

# find average of NumPy arrays
avg = (arr1 + arr2) / 2

print("Average of NumPy arrays:\n",
      avg)
```

**输出:**

```py
Average of NumPy arrays:
 [2\. 2.]
```

**示例 2:** 计算两个给定 NumPy 2d 阵列的平均值

## 蟒蛇 3

```py
# import library
import numpy as np

#  create a numpy 2d-arrays
arr1 = np.array([[3, 4], [8, 2]])
arr2 = np.array([[1, 0], [6, 6]])

# find average of NumPy arrays
avg = (arr1 + arr2) / 2

print("Average of NumPy arrays:\n",
      avg)
```

**输出:**

```py
Average of NumPy arrays:
 [[2\. 2.]
 [7\. 4.]]
```
# 计算两个给定 NumPy 阵列的协方差矩阵

> 原文:[https://www . geeksforgeeks . org/计算两个给定 numpy 数组的协方差矩阵/](https://www.geeksforgeeks.org/compute-the-covariance-matrix-of-two-given-numpy-arrays/)

在 NumPy 中，借助 [numpy.cov()](https://www.geeksforgeeks.org/python-numpy-cov-function/) 计算两个给定数组的协方差矩阵。在这里，我们将传递两个数组，它将返回两个给定数组的协方差矩阵。

> ***语法:** numpy.cov(m，y=None，rowvar=True，bias=False，ddof=None，fw thres = None，aw rights = None)*

**例 1:**

## 蟒蛇

```
import numpy as np

array1 = np.array([0, 1, 1])
array2 = np.array([2, 2, 1])

# Original array1
print(array1)

# Original array2
print(array2)

# Covariance matrix
print("\nCovariance matrix of the said arrays:\n",
      np.cov(array1, array2))
```
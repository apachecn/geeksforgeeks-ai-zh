# 对 Numpy 数组的每 N 个元素求平均值

> 原文:[https://www . geeksforgeeks . org/numpy 数组每 n 个元素求平均值/](https://www.geeksforgeeks.org/averaging-over-every-n-elements-of-a-numpy-array/)

在本文中，我们将学习如何找到 NumPy 数组中每 n 个元素的平均值。为了完成我们的任务，我们将使用 NumPy 模块提供的一些内置方法，如下所示:

*   **numpy. average ()** Calculate the average value, that is, the sum of all numbers divided by the number of elements.
*   [**numpy. rescale ()**](https://www.geeksforgeeks.org/numpy-reshape-python/) Take n elements at a time to reshape the array without changing the original data.
*   [**NumPy。**](https://www.geeksforgeeks.org/numpy-mean-in-python/) 意思是()

****例 1:平均过一个** **1-D 阵****

**T5

## 蟒 3

T8****T10】

```py
import numpy as np

# converting list to numpy array
givenArray = np.array([6, 5, 4, 3, 2, 1, 9,
                       8, 7, 12, 11, 10, 15, 
                       14, 13])

# here we took 3 as our input
n = 3

# calculates the average
avgResult = np.average(givenArray.reshape(-1, n), axis=1)

print("Given array:")
print(givenArray)

print("Averaging over every ", n, " elements of a numpy array:")
print(avgResult)
```**
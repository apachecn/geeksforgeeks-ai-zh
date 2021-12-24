# 如何在 NumPy 数组上映射函数？

> 原文:[https://www . geeksforgeeks . org/如何在 numpy 数组上映射函数/](https://www.geeksforgeeks.org/how-to-map-a-function-over-numpy-array/)

在本文中，我们将看到如何在 Python 中将函数映射到 NumPy 数组上。

## 方法 1: **numpy .矢量化()方法**

numpy.vectorize()函数将函数映射到包含一系列对象(如 numpy 数组)的数据结构上。对象或 NumPy 数组的嵌套序列作为输入，并返回单个 NumPy 数组或 NumPy 数组的元组。

## 蟒 3

```
import numpy as np

arr = np.array([1, 2, 3, 4, 5])

def addTwo(i):
    return i+2

applyall = np.vectorize(addTwo)
res = applyall(arr)
print(res)
```
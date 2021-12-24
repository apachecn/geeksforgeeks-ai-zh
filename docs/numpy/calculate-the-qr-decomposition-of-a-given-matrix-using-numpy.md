# 使用 NumPy

计算给定矩阵的 QR 分解

> 原文:[https://www . geeksforgeeks . org/计算给定矩阵的 qr 分解使用-numpy/](https://www.geeksforgeeks.org/calculate-the-qr-decomposition-of-a-given-matrix-using-numpy/)

在本文中，我们将讨论 **QR 分解** 的一个矩阵。矩阵的二维码分解是将一个矩阵分解成“A =二维码”，其中 Q 是正交的，R 是上三角矩阵。我们可以借助 numpy.linalg.qr()计算给定矩阵的 QR 分解。

> ***语法:** numpy.linalg.qr(a，mode = ' reduced ')*
> 
> ***参数:***
> 
> *   ***A:** The matrix (m, n) to be decomposed.*
> *   ***mode:** It is optional. Yes:*

**例 1:**

## 蟒 3

```py
import numpy as np

# Original matrix
matrix1 = np.array([[1, 2, 3], [3, 4, 5]])
print(matrix1)

# Decomposition of the said matrix
q, r = np.linalg.qr(matrix1)
print('\nQ:\n', q)
print('\nR:\n', r)
```
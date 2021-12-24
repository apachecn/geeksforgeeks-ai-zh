# 评估两个多维 NumPy 阵列的爱因斯坦求和惯例

> 原文:[https://www . geesforgeks . org/evaluate-einsteins-summary-conventi on-two-多维-numpy-arrays/](https://www.geeksforgeeks.org/evaluate-einsteins-summation-convention-of-two-multidimensional-numpy-arrays/)

在 Python 中，我们可以使用 NumPy 包的 [einsum()](https://www.geeksforgeeks.org/numpy-einsum-method/) 函数来计算两个给定多维数组的爱因斯坦求和约定。

> **语法:** numpy.einsum(下标，*操作数，out=None)
> 
> **参数:**
> 
> **下标:str**
> 
> 将求和下标指定为以逗号分隔的下标标签列表。除非包含明确的指示器“->”以及精确输出形式的下标标签，否则将执行隐式(经典爱因斯坦求和)计算。
> 
> **操作数:**类数组列表
> 
> 这些是操作的数组。
> 
> **out :** ndarray，可选
> 
> 如果提供，计算将在此数组中完成。
> 
> **返回:**基于爱因斯坦求和约定的计算。

**例 1:** 两个 2X2 矩阵的爱因斯坦求和约定

## 蟒蛇 3

```py
# Importing library
import numpy as np

# Creating two 2X2 matrix
matrix1 = np.array([[1, 2], [0, 2]])
matrix2 = np.array([[0, 1], [3, 4]])

print("Original matrix:")
print(matrix1)
print(matrix2)

# Output
result = np.einsum("mk,kn", matrix1, matrix2)

print("Einstein’s summation convention of the two matrix:")
print(result)
```

**输出:**

```py
Original matrix:
[[1 2]
 [0 2]]
[[0 1]
 [3 4]]
Einstein’s summation convention of the two matrix:
[[6 9]
 [6 8]]

```

**例 2:** 两个 3X3 矩阵的爱因斯坦求和约定

## 蟒蛇 3

```py
# Importing library
import numpy as np

# Creating two 3X3 matrix
matrix1 = np.array([[2, 3, 5], [4, 0, 2], [0, 6, 8]])
matrix2 = np.array([[0, 1, 5], [3, 4, 4], [8, 3, 0]])

print("Original matrix:")
print(matrix1)
print(matrix2)

# Output
result = np.einsum("mk,kn", matrix1, matrix2)

print("Einstein’s summation convention of the two matrix:")
print(result)
```

**输出:**

```py
Original matrix:
[[2 3 5]
 [4 0 2]
 [0 6 8]]
[[0 1 5]
 [3 4 4]
 [8 3 0]]
Einstein’s summation convention of the two matrix:
[[49 29 22]
 [16 10 20]
 [82 48 24]]

```

**例 3:** 两个 4X4 矩阵的爱因斯坦求和约定

## 蟒蛇 3

```py
# Importing library
import numpy as np

# Creating two 4X4 matrix
matrix1 = np.array([[1, 2, 3, 5], [4, 4, 0, 2], 
                    [0, 1, 6, 8], [0, 5, 6, 9]])

matrix2 = np.array([[0, 1, 9, 2], [3, 3, 4, 4], 
                    [1, 8, 3, 0], [5, 2, 1, 6]])

print("Original matrix:")
print(matrix1)
print(matrix2)

# Output
result = np.einsum("mk,kn", matrix1, matrix2)

print("Einstein’s summation convention of the two matrix:")
print(result)
```

**输出:**

```py
Original matrix:
[[1 2 3 5]
 [4 4 0 2]
 [0 1 6 8]
 [0 5 6 9]]
[[0 1 9 2]
 [3 3 4 4]
 [1 8 3 0]
 [5 2 1 6]]
Einstein’s summation convention of the two matrix:
[[34 41 31 40]
 [22 20 54 36]
 [49 67 30 52]
 [66 81 47 74]]

```
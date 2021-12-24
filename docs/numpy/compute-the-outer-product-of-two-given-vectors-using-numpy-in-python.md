# 使用 Python 中的 NumPy 计算两个给定向量的外积

> 原文:[https://www . geeksforgeeks . org/使用 python 中的 numpy 计算两个给定向量的外积/](https://www.geeksforgeeks.org/compute-the-outer-product-of-two-given-vectors-using-numpy-in-python/)

在 Python 中，我们可以使用 NumPy 包的 [outer()](https://www.geeksforgeeks.org/numpy-outer-function-python/) 函数来求两个矩阵的外积。

> **语法:** numpy.outer(a，b，out =无)
> 
> **参数:**
> 
> **a:**【array _ like】第一个输入向量。如果输入还不是一维的，则将其展平。
> 
> **b:**【array _ like】第二个输入向量。如果输入还不是一维的，则将其展平。
> 
> **out:**【n 数组，可选】存储结果的位置。
> 
> **返回:**【ndarray】返回两个向量的外积。out[i，j] = a[i] * b[j]

**例 1:** 一维数组的外积

## 蟒蛇 3

```
# Importing library
import numpy as np

# Creating two 1-D arrays
array1 = np.array([6,2])
array2 = np.array([2,5])
print("Original 1-D arrays:")
print(array1)
print(array2)

# Output
print("Outer Product of the two array is:")
result = np.outer(array1, array2)
print(result)
```

**输出:**

```
Original 1-D arrays:
[6 2]
[2 5]
Outer Product of the two array is:
[[12 30]
 [ 4 10]]

```

**例 2:**2 x2 矩阵的外积

## 蟒蛇 3

```
# Importing library
import numpy as np

# Creating two 2-D matrix
matrix1 = np.array([[1, 3], [2, 6]])
matrix2 = np.array([[0, 1], [1, 9]])
print("Original 2-D matrix:")
print(matrix1)
print(matrix2)

# Output
print("Outer Product of the two matrix is:")
result = np.outer(matrix1, matrix2)
print(result)
```

**输出:**

```
Original 2-D matrix:
[[1 3]
 [2 6]]
[[0 1]
 [1 9]]
Outer Product of the two matrix is:
[[ 0  1  1  9]
 [ 0  3  3 27]
 [ 0  2  2 18]
 [ 0  6  6 54]]

```

**例 3:**3x 3 矩阵的外积

## 蟒蛇 3

```
# Importing library
import numpy as np

# Creating two 3-D matrix
matrix1 = np.array([[2, 8, 2], [3, 4, 8], [0, 2, 1]])
matrix2 = np.array([[2, 1, 1], [0, 1, 0], [2, 3, 0]])
print("Original 3-D matrix:")
print(matrix1)
print(matrix2)

# Output
print("Outer Product of the two matrix is:")
result = np.outer(matrix1, matrix2)
print(result)
```

**输出:**

```
Original 3-D matrix:
[[2 8 2]
 [3 4 8]
 [0 2 1]]
[[2 1 1]
 [0 1 0]
 [2 3 0]]
Outer Product of the two matrix is:
[[ 4  2  2  0  2  0  4  6  0]
 [16  8  8  0  8  0 16 24  0]
 [ 4  2  2  0  2  0  4  6  0]
 [ 6  3  3  0  3  0  6  9  0]
 [ 8  4  4  0  4  0  8 12  0]
 [16  8  8  0  8  0 16 24  0]
 [ 0  0  0  0  0  0  0  0  0]
 [ 4  2  2  0  2  0  4  6  0]
 [ 2  1  1  0  1  0  2  3  0]]

```
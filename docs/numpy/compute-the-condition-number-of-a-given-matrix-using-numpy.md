# 使用 NumPy

计算给定矩阵的条件数

> 原文:[https://www . geeksforgeeks . org/计算给定矩阵的条件数-使用-numpy/](https://www.geeksforgeeks.org/compute-the-condition-number-of-a-given-matrix-using-numpy/)

在本文中，我们将使用 NumPy 包的 cond()函数来计算给定矩阵的条件数。cond()是 NumPy 包中线性代数模块的函数。

**语法:**

```
numpy.linalg.cond(x, p=None)
```

**例 1:**2 x2 矩阵的条件数

## 蟒蛇 3

```
# Importing library
import numpy as np

# Creating a 2X2 matrix
matrix = np.array([[4, 2], [3, 1]])

print("Original matrix:")
print(matrix)

# Output
result =  np.linalg.cond(matrix)

print("Condition number of the matrix:")
print(result)
```

**输出:**

```
Original matrix:
[[4 2]
 [3 1]]
Condition number of the matrix:
14.933034373659256

```

**例 2:**3x 3 矩阵的条件数

## 蟒蛇 3

```
# Importing library
import numpy as np

# Creating a 3X3 matrix
matrix = np.array([[4, 2, 0], [3, 1, 2], [1, 6, 4]])

print("Original matrix:")
print(matrix)

# Output
result =  np.linalg.cond(matrix)

print("Condition number of the matrix:")
print(result)
```

**输出:**

```
Original matrix:
[[4 2 0]
 [3 1 2]
 [1 6 4]]
Condition number of the matrix:
5.347703616656448

```

**例 3:**4x 4 矩阵的条件数

## 蟒蛇 3

```
# Importing library
import numpy as np

# Creating a 4X4 matrix
matrix = np.array([[4, 1, 4, 2], [3, 1, 2, 0], 
                   [3, 5, 7 ,1], [0, 6, 8, 4]])

print("Original matrix:")
print(matrix)

# Output
result =  np.linalg.cond(matrix)

print("Condition number of the matrix:")
print(result)
```

**输出:**

```
Original matrix:
[[4 1 4 2]
 [3 1 2 0]
 [3 5 7 1]
 [0 6 8 4]]
Condition number of the matrix:
57.34043866386226

```
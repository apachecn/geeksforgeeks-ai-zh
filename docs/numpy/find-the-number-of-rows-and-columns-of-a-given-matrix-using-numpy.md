# 使用 NumPy

计算给定矩阵的行数和列数

> 原文:[https://www . geeksforgeeks . org/find-给定矩阵的行数和列数-使用-numpy/](https://www.geeksforgeeks.org/find-the-number-of-rows-and-columns-of-a-given-matrix-using-numpy/)

在 [NumPy](https://www.geeksforgeeks.org/numpy-in-python-set-1-introduction/) 中借助 **shape()函数**、**T5】我们可以找到行数和列数。在这个函数中，我们传递一个矩阵，它将返回矩阵的行号和列号。**

**语法:**

```py
shape()
```

**返回:**行数和列数。

**例:**

## 蟒蛇

```py
import numpy as np

matrix= np.arange(1,9).reshape((3, 3))

# Original matrix
print(matrix)

# Number of rows and columns of the said matrix
print(matrix.shape)
```

**输出:**

```py
[[1 2 3]
[4 5 6]
[7 8 9]]
(3,3)

```

**例:**

## 蟒蛇

```py
import numpy as np

matrix= np.arange(10,15).reshape((3, 2))

# Original matrix:
print(matrix)

# Number of rows and columns of the said matrix
print(matrix.shape)
```

**输出**

```py
[[10 11]
[12 13]
[14 15]]
(3,2)

```
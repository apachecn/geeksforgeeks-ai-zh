# NumPy 中的矩阵乘法

> 原文:[https://www . geeksforgeeks . org/matrix-乘法 in-numpy/](https://www.geeksforgeeks.org/matrix-multiplication-in-numpy/)

让我们看看如何用 NumPy 计算矩阵乘法。我们将使用 [numpy.dot()](https://www.geeksforgeeks.org/numpy-dot-python/) 方法来求 2 个矩阵的乘积。

```py
For example, for two matrices A and B.
A = [[1, 2], [2, 3]]
B = [[4, 5], [6, 7]]

So, A.B = [[1*4 + 2*6, 2*4 + 3*6], [1*5 + 2*7, 2*5 + 3*7]
So the computed answer will be: [[16, 26], [19, 31]]

```

在 Python 中，numpy.dot()方法用于计算两个数组之间的点积。

**例 1:**2 个方阵的矩阵乘法。

```py
# importing the module
import numpy as np

# creating two matrices
p = [[1, 2], [2, 3]]
q = [[4, 5], [6, 7]]
print("Matrix p :")
print(p)
print("Matrix q :")
print(q)

# computing product
result = np.dot(p, q)

# printing the result
print("The matrix multiplication is :")
print(result)
```

**输出:**

```py
Matrix p :
[[1, 2], [2, 3]]
Matrix q :
[[4, 5], [6, 7]]
The matrix multiplication is :
[[16 19]
 [26 31]]

```

**例 2:**2 个矩形矩阵的矩阵乘法。

```py
# importing the module
import numpy as np

# creating two matrices
p = [[1, 2], [2, 3], [4, 5]]
q = [[4, 5, 1], [6, 7, 2]]
print("Matrix p :")
print(p)
print("Matrix q :")
print(q)

# computing product
result = np.dot(p, q)

# printing the result
print("The matrix multiplication is :")
print(result)
```

**输出:**

```py
Matrix p :
[[1, 2], [2, 3], [4, 5]]
Matrix q :
[[4, 5, 1], [6, 7, 2]]
The matrix multiplication is :
[[16 19  5]
 [26 31  8]
 [46 55 14]]

```
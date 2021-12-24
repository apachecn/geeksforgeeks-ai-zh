# 如何用 NumPY 计算给定方阵的特征值和右特征向量？

> 原文:[https://www . geeksforgeeks . org/如何使用-numpy/](https://www.geeksforgeeks.org/how-to-compute-the-eigenvalues-and-right-eigenvectors-of-a-given-square-array-using-numpy/) 计算给定方阵的特征值和右特征向量

在本文中，我们将讨论如何使用 NumPy 库计算给定方阵的特征值和右特征向量。

**示例:**

```
Suppose we have a matrix as: 
[[1,2],
[2,3]] 

Eigenvalue we get from this matrix or square array is: 
[-0.23606798 4.23606798]

Eigenvectors of this matrix are: 
[[-0.85065081 -0.52573111], 
[ 0.52573111 -0.85065081]] 
```

要知道它们是如何被数学计算的，请看这个[**特征值和特征向量的计算**。](https://www.geeksforgeeks.org/eigen-values-and-eigen-vectors/)在下面的例子中，我们使用了[**numpy . linalg . EIG()**](https://www.geeksforgeeks.org/numpy-linalg-eig-method-in-python/)来寻找给定方阵的特征值和特征向量。

> **语法:** numpy.linalg.eig()
> 
> **参数:**一个方阵。
> 
> **Return:** 它会返回两个值第一个是特征值，第二个是特征向量。

**例 1:**

## 蟒蛇 3

```
# importing numpy library
import numpy as np

# create numpy 2d-array
m = np.array([[1, 2],
              [2, 3]])

print("Printing the Original square array:\n",
      m)

# finding eigenvalues and eigenvectors
w, v = np.linalg.eig(m)

# printing eigen values
print("Printing the Eigen values of the given square array:\n",
      w)

# printing eigen vectors
print("Printing Right eigenvectors of the given square array:\n"
      v)
```

**输出:**

```
Printing the Original square array:
 [[1 2]
 [2 3]]
Printing the Eigen values of the given square array:
 [-0.23606798  4.23606798]
Printing Right eigenvectors of the given square array:
 [[-0.85065081 -0.52573111]
 [ 0.52573111 -0.85065081]]
```

**例 2:**

## 蟒蛇 3

```
# importing numpy library
import numpy as np

# create numpy 2d-array
m = np.array([[1, 2, 3],
              [2, 3, 4],
              [4, 5, 6]])

print("Printing the Original square array:\n",
      m)

# finding eigenvalues and eigenvectors
w, v = np.linalg.eig(m)

# printing eigen values
print("Printing the Eigen values of the given square array:\n",
      w)

# printing eigen vectors
print("Printing Right eigenvectors of the given square array:\n",
      v)
```

**输出:**

```
Printing the Original square array:
 [[1 2 3]
 [2 3 4]
 [4 5 6]]
Printing the Eigen values of the given square array:
 [ 1.08309519e+01 -8.30951895e-01  1.01486082e-16]
Printing Right eigenvectors of the given square array:
 [[ 0.34416959  0.72770285  0.40824829]
 [ 0.49532111  0.27580256 -0.81649658]
 [ 0.79762415 -0.62799801  0.40824829]]
```
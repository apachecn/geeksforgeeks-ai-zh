# 使用 NumPy

找到矩阵或向量范数

> 原文:[https://www . geeksforgeeks . org/find-a-matrix-or-vector-norm-use-numpy/](https://www.geeksforgeeks.org/find-a-matrix-or-vector-norm-using-numpy/)

为了找到矩阵或向量范数，我们使用 Python 库 numpy 的函数 numpy.linalg.norm()。该函数根据其参数值返回七个矩阵范数之一或无限向量范数之一。

> **语法:** numpy.linalg.norm(x，ord = None，axis=None)
> **参数:**
> **x:** 输入
> **order:**norm 的顺序
> **axis:** None，返回向量或矩阵范数，如果是整数值，则指定向量范数将沿其计算的 x 轴

**例 1:**

## 蟒蛇 3

```py
# import library
import numpy as np

# initialize vector
vec = np.arange(10)

# compute norm of vector
vec_norm = np.linalg.norm(vec)

print("Vector norm:")
print(vec_norm)
```

**输出:**

```py
Vector norm:
16.881943016134134
```

上述代码计算维度为(1，10)
**的向量的向量范数。示例 2:**

## 蟒蛇 3

```py
# import library
import numpy as np

# initialize matrix
mat = np.array([[ 1, 2, 3],
               [4, 5, 6]])

# compute norm of matrix
mat_norm = np.linalg.norm(mat)

print("Matrix norm:")
print(mat_norm)
```

**输出:**

```py
Matrix norm:
9.539392014169456
```

这里，我们得到维度(2，3)
**的矩阵的矩阵范数。例 3:**
计算沿特定轴的矩阵范数–

## 蟒蛇 3

```py
# import library
import numpy as np

mat = np.array([[ 1, 2, 3],
               [4, 5, 6]])

# compute matrix num along axis
mat_norm = np.linalg.norm(mat, axis = 1)

print("Matrix norm along particular axis :")
print(mat_norm)
```

**输出:**

```py
Matrix norm along particular axis :
[3.74165739 8.77496439]
```

该代码生成一个矩阵范数，输出也是形状(1，2)
**的矩阵示例 4:**

## 蟒蛇 3

```py
# import library
import numpy as np

# initialize vector
vec = np.arange(9)

# convert vector into matrix
mat = vec.reshape((3, 3))

# compute norm of vector
vec_norm = np.linalg.norm(vec)

print("Vector norm:")
print(vec_norm)

# computer norm of matrix
mat_norm = np.linalg.norm(mat)

print("Matrix norm:")
print(mat_norm)
```

**输出:**

```py
Vector norm:
14.2828568570857
Matrix norm:
14.2828568570857
```

从上面的输出，很明显，如果我们把一个向量转换成一个矩阵，或者如果两个向量都有相同的元素，那么它们的范数也是相等的。
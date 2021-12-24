# numpy 矩阵运算|恒等式()函数

> 原文:[https://www . geesforgeks . org/numpy-matrix-operations-identity-function/](https://www.geeksforgeeks.org/numpy-matrix-operations-identity-function/)

**`numpy.matlib.identity()`** 是 numpy 中做矩阵运算的另一个功能。它返回给定输入大小的平方单位矩阵。

> **语法:** numpy.matlib.identity(n，dtype=None)
> 
> **参数:**
> **n:**【int】输出矩阵的行数和列数。
> **数据类型:**【可选】所需输出数据类型。
> 
> **返回:**n×n 矩阵，主对角线设为 1，其他元素均为零。

**代码#1 :**

```py
# Python program explaining
# numpy.matlib.identity() function

# importing matrix library from numpy
import numpy as geek
import numpy.matlib

# desired 3 x 3 output square identity matrix 
out_mat = geek.matlib.identity(3) 
print ("Output matrix : ", out_mat) 
```

**Output :**

```py
Output matrix :  
[[ 1\.  0\.  0.]
 [ 0\.  1\.  0.]
 [ 0\.  0\.  1.]]

```

**代码#2 :**

```py
# Python program explaining
# numpy.matlib.identity() function

# importing numpy and matrix library
import numpy as geek
import numpy.matlib

# desired 5 x 5 output square identity matrix 
out_mat = geek.matlib.identity(n = 5, dtype = int) 
print ("Output matrix : ", out_mat) 
```

**Output :**

```py
Output matrix :  
[[1 0 0 0 0]
 [0 1 0 0 0]
 [0 0 1 0 0]
 [0 0 0 1 0]
 [0 0 0 0 1]]

```
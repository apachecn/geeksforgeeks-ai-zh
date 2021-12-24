# numpy 矩阵运算| eye()功能

> 原文:[https://www . geesforgeks . org/numpy-matrix-operations-eye-function/](https://www.geeksforgeeks.org/numpy-matrix-operations-eye-function/)

**`numpy.matlib.eye()`** 是 numpy 中做矩阵运算的另一个功能。它返回一个对角线上为 1，其他地方为 0 的矩阵。

> **语法:** numpy.matlib.eye(n，M=None，k=0，dtype='float '，order='C ')
> 
> **参数:**
> **n:**【int】输出矩阵的行数。
> **M:**【int，可选】输出矩阵的列数，默认为 n .
> **k:**【int，可选】对角线的索引。0 表示主对角线，正值表示上对角线，负值表示下对角线。默认值为 0。
> **数据类型:**【可选】所需的输出数据类型。
> **顺序:**在内存中是按行-主(C 风格)还是列-主(Fortran 风格)顺序存储多维数据。
> 
> **返回:**n×M 的矩阵，其中所有元素都等于零，除了第 k 个对角线，其值等于 1。

**代码#1 :**

```
# Python program explaining
# numpy.matlib.eye() function

# importing matrix library from numpy
import numpy as geek
import numpy.matlib

# desired 3 x 3 output matrix 
out_mat = geek.matlib.eye(3, k = 0) 
print ("Output matrix : ", out_mat) 
```

**Output :**

```
Output matrix :  
[[ 1\.  0\.  0.]
 [ 0\.  1\.  0.]
 [ 0\.  0\.  1.]]

```

**代码#2 :**

```
# Python program explaining
# numpy.matlib.eye() function

# importing numpy and matrix library
import numpy as geek
import numpy.matlib

# desired 4 x 5 output matrix 
out_mat = geek.matlib.eye(n = 4, M = 5, k = 1, dtype = int) 
print ("Output matrix : ", out_mat) 
```

**Output :**

```
Output matrix :  
[[0 1 0 0 0]
 [0 0 1 0 0]
 [0 0 0 1 0]
 [0 0 0 0 1]]

```
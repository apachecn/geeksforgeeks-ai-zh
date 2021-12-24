# numpy 矩阵运算|零()函数

> 原文:[https://www . geesforgeks . org/numpy-matrix-operations-zero-function/](https://www.geeksforgeeks.org/numpy-matrix-operations-zeros-function/)

**`numpy.matlib.zeros()`** 是 numpy 中做矩阵运算的另一个功能。它返回给定形状和类型的矩阵，用零填充。

> **语法:** numpy.matlib.zeros(shape，dtype=None，order='C ')
> 
> **参数:**
> **形状:**【int，int】输出矩阵的行数和列数。如果形状的长度为 1(即，N)，或者是标量 N，则 out 成为形状(1，N)的单行矩阵。
> **数据类型:**【可选】所需输出数据类型。
> **顺序:**在内存中是按行-主(C 风格)还是列-主(Fortran 风格)顺序存储多维数据。
> 
> **返回:**给定形状、数据类型和顺序的零矩阵。

**代码#1 :**

```py
# Python program explaining
# numpy.matlib.zeros() function

# importing matrix library from numpy
import numpy as geek
import numpy.matlib

# desired 3 x 4 zero output matrix 
out_mat = geek.matlib.zeros((3, 4)) 
print ("Output matrix : ", out_mat) 
```

**Output :**

```py
Output matrix :  [[ 0\.  0\.  0\.  0.]
 [ 0\.  0\.  0\.  0.]
 [ 0\.  0\.  0\.  0.]]

```

**代码#2 :**

```py
# Python program explaining
# numpy.matlib.zeros() function

# importing numpy and matrix library
import numpy as geek
import numpy.matlib

# desired 1 x 5 zero output matrix 
out_mat = geek.matlib.zeros(shape = 5, dtype = int) 
print ("Output matrix : ", out_mat) 
```

**Output :**

```py
Output matrix :  [[0 0 0 0 0]]

```
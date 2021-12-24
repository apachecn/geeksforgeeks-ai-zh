# numpy 矩阵运算|空()函数

> 原文:[https://www . geesforgeks . org/numpy-matrix-operations-empty-function/](https://www.geeksforgeeks.org/numpy-matrix-operations-empty-function/)

**`numpy.matlib.empty()`** 是 numpy 中做矩阵运算的另一个功能。它返回给定形状和类型的新矩阵，而不初始化条目。

> **语法:** numpy.matlib.empty(shape，dtype=None，order='C ')
> 
> **参数:**
> **形状:**【int 或 int 的元组】所需输出空矩阵的形状。
> **数据类型:**【可选】所需输出数据类型。
> **顺序:**在内存中是按行-主(C 风格)还是列-主(Fortran 风格)顺序存储多维数据。
> 
> **返回:**给定形状和类型的新矩阵，

**代码#1 :**

```py
# Python program explaining
# numpy.matlib.empty() function

# importing numpy and matrix library
import numpy as geek
import numpy.matlib

# desired output matrix 
out_mat = geek.matlib.empty((2, 3)) 
print ("Output matrix : ", out_mat) 
```

**Output :**

```py
Output matrix :  [[  6.93621940e-310   2.43141878e-316   6.93621669e-310]
 [  6.93621669e-310   6.93621553e-310   6.93621553e-310]]

```

**代码#2 :**

```py
# Python program explaining
# numpy.matlib.empty() function

# importing numpy and matrix library
import numpy as geek
import numpy.matlib

# desired output matrix 
out_mat = geek.matlib.empty((2, 3), dtype = int, order = 'C') 
print ("Output matrix : ", out_mat) 
```

**Output :**

```py
Output matrix :  [[140133380791224 140133380791224 140133356100528]
 [140133356100336 140133356100592 140133343343704]]

```
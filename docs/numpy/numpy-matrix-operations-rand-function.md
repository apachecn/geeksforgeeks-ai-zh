# numpy 矩阵运算| rand()函数

> 原文:[https://www . geesforgeks . org/numpy-matrix-operations-rand-function/](https://www.geeksforgeeks.org/numpy-matrix-operations-rand-function/)

**`numpy.matlib.rand()`** 是 numpy 中做矩阵运算的另一个功能。它返回给定形状的[0，1]上均匀分布的随机值矩阵。

> **语法:**num py . MATLAB . rand(* args)
> 
> **参数:**
> ***参数:**【参数】输出矩阵的形状。如果给定 N 个整数，每个整数指定一个维度的大小。如果作为元组给出，这个元组给出完整的形状。如果有多个参数，并且第一个参数是元组，则忽略其他参数。
> 
> **返回:**随机值的矩阵。

**代码#1 :**

```py
# Python program explaining
# numpy.matlib.rand() function

# importing matrix library from numpy
import numpy as geek
import numpy.matlib

# desired 3 x 4 random output matrix 
out_mat = geek.matlib.rand((3, 4)) 
print ("Output matrix : ", out_mat) 
```

**Output :**

```py
Output matrix :  [[ 0.37976085  0.68700838  0.83898103  0.72073804]
 [ 0.80577587  0.2508264   0.30179229  0.81376797]
 [ 0.70202528  0.17830863  0.61509844  0.27758369]]

```

**代码#2 :**

```py
# Python program explaining
# numpy.matlib.rand() function

# importing numpy and matrix library
import numpy as geek
import numpy.matlib

# desired 1 x 5 random output matrix 
out_mat = geek.matlib.rand(5) 
print ("Output matrix : ", out_mat) 
```

**Output :**

```py
Output matrix :  [[ 0.56138247  0.97881105  0.53380995  0.27486091  0.1603695 ]]

```

**代码#3 :**

```py
# Python program explaining
# numpy.matlib.rand() function

# importing numpy and matrix library
import numpy as geek
import numpy.matlib

# more than one argument given
out_mat = geek.matlib.rand((5, 3), 4) 
print ("Output matrix : ", out_mat) 
```

**Output :**

```py
Output matrix :  [[ 0.86770893  0.35628104  0.19744129]
 [ 0.90376689  0.58349554  0.9830152 ]
 [ 0.64711739  0.09531791  0.17555793]
 [ 0.66141287  0.09164568  0.28818979]
 [ 0.92225364  0.56779388  0.58498534]]

```
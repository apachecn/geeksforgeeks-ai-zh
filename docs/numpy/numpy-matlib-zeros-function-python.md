# numpy.matlib.zeros()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-matlib-zeros-function-python/](https://www.geeksforgeeks.org/numpy-matlib-zeros-function-python/)

**`numpy.matlib.zeros()`** 函数返回给定形状和类型的矩阵，用零填充。

> **语法:** numpy.matlib.zeros(shape，dtype = None，order = 'C')
> **参数:**
> **形状:**【ints 序列】空矩阵的形状。
> **数据类型:**【数据类型，可选】矩阵所需的数据类型，默认为 float。
> **顺序:** [{'C '，' F'}，可选]是以 C-还是 Fortran-连续顺序存储结果，默认为' C '。
> **返回:**【矩阵】给定形状、数据类型和顺序的零矩阵。

**代码#1 :**

```
# Python program explaining
# numpy.matlib.zeros() function

# importing numpy as geek 
# and importing matlib module  
import numpy as geek
import numpy.matlib

gfg = geek.matlib.zeros((3, 3))

print (gfg)
```

**输出:**

```
[[ 0\.  0\.  0.]
 [ 0\.  0\.  0.]
 [ 0\.  0\.  0.]]

```

**代码#2 :**

```
# Python program explaining
# numpy.matlib.zeros() function

# importing numpy as geek 
# and importing matlib module  
import numpy as geek
import numpy.matlib

gfg = geek.matlib.zeros(4)

print (gfg)
```

**输出:**

```
[[ 0\.  0\.  0\.  0.]]

```
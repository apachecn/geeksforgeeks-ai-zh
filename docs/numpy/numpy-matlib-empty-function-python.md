# numpy.matlib.empty()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-matlib-empty-function-python/](https://www.geeksforgeeks.org/numpy-matlib-empty-function-python/)

**`numpy.matlib.empty()`** 函数返回给定形状和类型的新矩阵，不初始化条目。

> **语法:** numpy.matlib.empty(shape，dtype = None，order = 'C')
> **参数:**
> **shape:**【int 或 int 的元组】空矩阵的 Shape。
> **数据类型:**【数据类型，可选】所需输出数据类型。
> **顺序:**【{ ' C '，' F'}，可选】内存中是按行-主(C 风格)还是列-主(Fortran 风格)顺序存储多维数据。
> **返回:**【矩阵】给定形状和类型的新矩阵，不初始化条目。

**代码#1 :**

```py
# Python program explaining
# numpy.matlib.empty() function

# importing numpy as geek 
# and importing matlib module  
import numpy as geek
import numpy.matlib

# filled with random data
gfg = geek.matlib.empty((2, 2))

# output will be random
print (gfg)
```

**输出:**

```py
[[  6.91957648e-310   1.90383493e-316]
 [  6.91957669e-310   5.30409905e-317]]

```

**代码#2 :**

```py
# Python program explaining
# numpy.matlib.empty() function

# importing numpy as geek 
# and importing matlib module  
import numpy as geek
import numpy.matlib

# filled with random data
gfg = geek.matlib.empty((2, 2), dtype = int)

# output will be random
print (gfg)
```

**输出:**

```py
[[139855860099992        40294208]
 [139855825297024        10730496]]

```
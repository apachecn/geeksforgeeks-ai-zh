# Numpy 矩阵。I 功能| Python

> 原文:[https://www . geeksforgeeks . org/numpy-matrix-I-function-python/](https://www.geeksforgeeks.org/numpy-matrix-i-function-python/)

借助 **`numpy.matrix.I()`** 函数，我们可以得到与给定矩阵相同大小的乘法逆。

> **语法:** numpy.matrix.I()
> 
> **返回:**【矩阵对象】如果 self 非奇异，ret 是这样的:ret * self = = self * ret = = NP . matrix(NP . eye(self[0，])。大小)都返回真。返回给定矩阵的乘法逆。

**代码#1 :**

```
# Python program explaining
# numpy.matrix.I() function

# importing numpy as geek 
import numpy as geek 

mat = geek.matrix('[3, 4; 5, 6]') 

# applying matrix.getI() method 
gfg = mat.getI() 

print(gfg)
```

**输出:**

```
[[-3\.   2\. ]
 [ 2.5 -1.5]]

```

**代码#2 :**

```
# Python program explaining
# numpy.matrix.I() function

# importing numpy as geek 
import numpy as geek 

mat = geek.matrix('[1, 2, 3; 4, 5, 6; 7, 8, 9]') 

# applying matrix.getI() method 
gfg = mat.getI() 

print(gfg)
```

**输出:**

```
[[ -4.50359963e+15   9.00719925e+15  -4.50359963e+15]
 [  9.00719925e+15  -1.80143985e+16   9.00719925e+15]
 [ -4.50359963e+15   9.00719925e+15  -4.50359963e+15]]

```
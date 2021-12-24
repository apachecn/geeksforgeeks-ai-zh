# numpy.matrix.A()函数–Python

> 原文:[https://www . geeksforgeeks . org/numpy-matrix-a-function-python/](https://www.geeksforgeeks.org/numpy-matrix-a-function-python/)

**`numpy.matrix.A()`** 函数返回自我作为一个数组对象。

> **语法:** numpy.matrix.A()
> 
> **参数:**无
> **返回:**【ndarray】作为 ndarray 返回自我。

**代码#1 :**

```
# Python program explaining
# numpy.matrix.A() function

# importing numpy as geek 
import numpy as geek 

mat = geek.matrix(geek.arange(9).reshape((3, 3)))

gfg = mat.getA()

print (gfg)
```

**输出:**

```
[[0 1 2]
 [3 4 5]
 [6 7 8]]

```

**代码#2 :**

```
# Python program explaining
# numpy.matrix.A() function

# importing numpy as geek 
import numpy as geek 

mat = geek.matrix(geek.arange(20).reshape((4, 5)))

gfg = mat.getA()

print (gfg)
```

**输出:**

```
[[ 0  1  2  3  4]
 [ 5  6  7  8  9]
 [10 11 12 13 14]
 [15 16 17 18 19]]

```
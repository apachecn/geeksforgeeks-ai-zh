# numpy . tril _ indexs()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-tril _ indexs-function-python/](https://www.geeksforgeeks.org/numpy-tril_indices-function-python/)

**`numpy.tril_indices()`** 函数返回一个(n，m)数组的下三角的指数。

> **语法:**numpy . tril _ indexes(n，k = 0，m =无)
> **参数:**
> **n:**【int】返回的索引将对其有效的数组的行维度。
> **k:**【int，可选】对角线偏移。
> **m:**【int，可选】返回的数组对其有效的数组的列维度。默认情况下，m 等于 n。
> **返回:**【数组元组】三角形的索引。返回的元组包含两个数组，每个数组都有一维的索引。

**代码#1 :**

```
# Python program explaining
# numpy.tril_indices() function

# importing numpy as geek 
import numpy as geek

gfg = geek.tril_indices(3)

print (gfg)
```

**输出:**

```
(array([0, 1, 1, 2, 2, 2]), array([0, 0, 1, 0, 1, 2]))

```

**代码#2 :**

```
# Python program explaining
# numpy.tril_indices() function

# importing numpy as geek 
import numpy as geek

gfg = geek.tril_indices(3, 2)

print (gfg)
```

**输出:**

```
(array([0, 0, 0, 1, 1, 1, 2, 2, 2]), array([0, 1, 2, 0, 1, 2, 0, 1, 2]))

```
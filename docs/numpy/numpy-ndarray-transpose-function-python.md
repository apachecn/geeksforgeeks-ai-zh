# Numpy ndarray .转置()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-ndarray-transpose-function-python/](https://www.geeksforgeeks.org/numpy-ndarray-transpose-function-python/)

**`numpy.ndarray.transpose()`** 函数返回轴换位的数组视图。
对于一维数组，这没有影响，因为转置向量只是同一个向量。对于二维数组，这是标准的矩阵转置。对于 n-D 数组，如果给定了轴，它们的顺序指示轴是如何排列的。如果未提供轴且 arr.shape = (i[0]，i[1]，… i[n-2]，i[n-1])，则 arr .转置()。shape = (i[n-1]，i[n-2]，… i[1]，i[0])。

> **语法:**num py . ndaarray . transponte(* axes)
> 
> **参数:**
> **轴:**【无，整数元组，或 n 个整数】无或无参数:反转轴的顺序。
> int 的元组:元组中第 j 位的 I 表示 arr 的第 I 轴变成 arr .转置()(的第 j 轴。
> n 个 ints:与相同 ints 的 n 元组相同(这种形式只是作为元组形式的“方便”替代)
> 
> **返回:**【ndarray】arr 视图，轴适当排列。

**代码#1 :**

```
# Python program explaining
# numpy.ndarray.transpose() function

# importing numpy as geek 
import numpy as geek

arr = geek.array([[5, 6], [7, 8]])

gfg = arr.transpose()

print( gfg )
```

**输出:**

```
[[5 7]
 [6 8]]

```

**代码#2 :**

```
# Python program explaining
# numpy.ndarray.transpose() function

# importing numpy as geek 
import numpy as geek

arr = geek.array([[5, 6], [7, 8]])

gfg = arr.transpose((1, 0))

print( gfg )
```

**输出:**

```
[[5 7]
 [6 8]]

```
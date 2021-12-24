# num py . vssplits()函数| Python

> 原文:[https://www.geeksforgeeks.org/numpy-vsplit-function-python/](https://www.geeksforgeeks.org/numpy-vsplit-function-python/)

**`numpy.vsplit()`** 函数将一个数组垂直拆分为多个子数组(逐行)。vsplit 相当于 axis=0 时的拆分(默认)，数组总是沿着第一个轴拆分，与数组维度无关。

> **语法:** numpy.vsplit(arr，indexs _ or _ sections)
> **参数:**
> **arr:**【ndarray】要分成子数组的数组。
> **indexes _ or _ sections:**【int 或 1-D 数组】如果 indexes _ or _ sections 为整数 N，数组将沿轴分成 N 个相等的数组。
> 如果 indices _ or _ sections 是排序整数的一维数组，则条目指示数组沿轴拆分的位置
> **返回:**【n 数组】子数组列表。

**代码#1 :**

```
# Python program explaining
# numpy.vsplit() function

# importing numpy as geek 
import numpy as geek

arr = geek.arange(9.0).reshape(3, 3)

gfg = geek.vsplit(arr, 1)

print (gfg)
```

**输出:**

```
[array([[ 0.,  1.,  2.],
       [ 3.,  4.,  5.],
       [ 6.,  7.,  8.]])]

```

**代码#2 :**

```
# Python program explaining
# numpy.vsplit() function

# importing numpy as geek 
import numpy as geek

arr = geek.arange(36.0).reshape(6, 6)

gfg = geek.vsplit(arr, 2)

print (gfg)
```

**输出:**

```
[array([[  0.,   1.,   2.,   3.,   4.,   5.],
       [  6.,   7.,   8.,   9.,  10.,  11.],
       [ 12.,  13.,  14.,  15.,  16.,  17.]]), array([[ 18.,  19.,  20.,  21.,  22.,  23.],
       [ 24.,  25.,  26.,  27.,  28.,  29.],
       [ 30.,  31.,  32.,  33.,  34.,  35.]])]

```
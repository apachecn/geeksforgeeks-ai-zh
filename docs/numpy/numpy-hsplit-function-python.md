# numpy.hsplit()函数| Python

> 原文:[https://www.geeksforgeeks.org/numpy-hsplit-function-python/](https://www.geeksforgeeks.org/numpy-hsplit-function-python/)

**`numpy.hsplit()`** 函数将一个数组水平拆分为多个子数组(按列)。hsplit 相当于 axis=1 时的拆分，数组总是沿着第二个轴拆分，与数组维度无关。

> **语法:** numpy.hsplit(arr，indexs _ or _ sections)
> **参数:**
> **arr:**【ndarray】要分成子数组的数组。
> **indexes _ or _ sections:**【int 或 1-D 数组】如果 indexes _ or _ sections 为整数 N，数组将沿轴分成 N 个相等的数组。
> 如果 indices _ or _ sections 是排序整数的一维数组，则条目指示数组沿轴拆分的位置
> **返回:**【n 数组】子数组列表。

**代码#1 :**

```
# Python program explaining
# numpy.hsplit() function

# importing numpy as geek 
import numpy as geek

arr = geek.arange(16.0).reshape(4, 4)

gfg = geek.hsplit(arr, 2)

print (gfg)
```

**输出:**

```
[array([[  0.,   1.],
       [  4.,   5.],
       [  8.,   9.],
       [ 12.,  13.]]), array([[  2.,   3.],
       [  6.,   7.],
       [ 10.,  11.],
       [ 14.,  15.]])]

```

**代码#2 :**

```
# Python program explaining
# numpy.hsplit() function

# importing numpy as geek 
import numpy as geek

arr = geek.arange(27.0).reshape(3, 3, 3)

gfg = geek.hsplit(arr, 1)

print (gfg)
```

**输出:**

```
[array([[[  0.,   1.,   2.],
        [  3.,   4.,   5.],
        [  6.,   7.,   8.]],

       [[  9.,  10.,  11.],
        [ 12.,  13.,  14.],
        [ 15.,  16.,  17.]],

       [[ 18.,  19.,  20.],
        [ 21.,  22.,  23.],
        [ 24.,  25.,  26.]]])]

```
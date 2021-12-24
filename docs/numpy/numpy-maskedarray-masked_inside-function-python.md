# Numpy maskedarray . masked _ inside()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-masked _ inside-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-masked_inside-function-python/)

在许多情况下，数据集可能是不完整的，或者被无效数据污染。例如，传感器可能未能记录数据，或者记录了无效值。`numpy.ma`模块通过引入屏蔽数组提供了一种解决这个问题的便捷方法。屏蔽数组是指可能缺少条目或条目无效的数组。

**`numpy.MaskedArray.masked_inside()`** 功能是用来在给定的区间内屏蔽一个数组。该功能是屏蔽的快捷方式，在区间`[v1, v2] (v1 <= arr <= v2)`内 arr 的条件为真。边界 v1 和 v2 可以按任意顺序给出。

> **语法:** `numpy.ma.masked_inside(arr, v1, v2, copy=True)`
> 
> **参数:**
> **arr:**【ndarray】输入我们要屏蔽的数组。
> **v1、v2:**【int】上下范围。
> **复制:**【bool】如果为真(默认)，在结果中复制一份 arr。如果为假，就地修改 arr 并返回视图。
> 
> **返回:**【屏蔽数组】屏蔽后的结果数组。

**代码#1 :**

```py
# Python program explaining
# numpy.MaskedArray.masked_inside() method 

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array 
in_arr = geek.array([1, 2, 3, -1, 2])
print ("Input array : ", in_arr)

# applying MaskedArray.masked_inside methods 
# to input array in the range[-1, 1]
mask_arr = ma.masked_inside(in_arr, -1, 1)
print ("Masked array : ", mask_arr)
```

**Output:**

```py
Input array :  [ 1  2  3 -1  2]
Masked array :  [-- 2 3 -- 2]

```

**代码#2 :**

```py
# Python program explaining
# numpy.MaskedArray.masked_inside() method 

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array 
in_arr = geek.array([5e8, 3e-5, -45.0, 4e4, 5e2])
print ("Input array : ", in_arr)

# applying MaskedArray.masked_inside methods 
# to input array in the range[5e2, 5e8]
mask_arr = ma.masked_inside(in_arr, 5e2, 5e8)
print ("Masked array : ", mask_arr)
```

**Output:**

```py
Input array :  [ 5.0e+08  3.0e-05 -4.5e+01  4.0e+04  5.0e+02]
Masked array :  [-- 3e-05 -45.0 -- --]

```
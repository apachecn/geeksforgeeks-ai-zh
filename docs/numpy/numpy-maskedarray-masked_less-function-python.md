# Numpy maskedarray . masked _ less()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-masked _ less-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-masked_less-function-python/)

在许多情况下，数据集可能是不完整的，或者被无效数据污染。例如，传感器可能未能记录数据，或者记录了无效值。`numpy.ma`模块通过引入屏蔽数组提供了一种解决这个问题的便捷方法。屏蔽数组是指可能缺少条目或条目无效的数组。

**`numpy.MaskedArray.masked_less()`** 函数用于屏蔽一个数组中小于给定值的地方。该功能是`masked_where`的快捷方式，有`condition = (arr < value).`

> **语法:** `numpy.ma.masked_less(arr, value, copy=True)`
> 
> **参数:**
> **arr:**【ndarray】输入我们要屏蔽的数组。
> **值:**【int】用于屏蔽为<值的数组元素。
> **复制:**【bool】如果为真(默认)，在结果中复制一份 arr。如果为假，就地修改 arr 并返回视图。
> 
> **返回:**【屏蔽数组】屏蔽后的结果数组。

**代码#1 :**

```
# Python program explaining
# numpy.MaskedArray.masked_less() method 

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array 
in_arr = geek.array([1, 2, 3, -1, 2])
print ("Input array : ", in_arr)

# applying MaskedArray.masked_less methods 
# to input array where value<2
mask_arr = ma.masked_less(in_arr, 2)
print ("Masked array : ", mask_arr)
```

**Output:**

```
Input array :  [ 1  2  3 -1  2]
Masked array :  [-- 2 3 -- 2]

```

**代码#2 :**

```
# Python program explaining
# numpy.MaskedArray.masked_less() method 

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array 
in_arr = geek.array([5e8, 3e-5, -45.0, 4e4, 5e2])
print ("Input array : ", in_arr)

# applying MaskedArray.masked_less methods 
# to input array where value<5e2
mask_arr = ma.masked_less(in_arr, 5e2)
print ("Masked array : ", mask_arr)
```

**Output:**

```
Input array :  [ 5.0e+08  3.0e-05 -4.5e+01  4.0e+04  5.0e+02]
Masked array :  [500000000.0 -- -- 40000.0 500.0]

```
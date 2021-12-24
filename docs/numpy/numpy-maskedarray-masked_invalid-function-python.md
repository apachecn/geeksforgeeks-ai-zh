# Numpy maskedarray . masked _ invalid()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-masked _ invalid-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-masked_invalid-function-python/)

在许多情况下，数据集可能是不完整的，或者被无效数据污染。例如，传感器可能未能记录数据，或者记录了无效值。`numpy.ma`模块通过引入屏蔽数组提供了一种解决这个问题的便捷方法。屏蔽数组是指可能缺少条目或条目无效的数组。

**`numpy.MaskedArray.masked_invalid()`** 函数用于屏蔽出现无效值的数组。该功能是`masked_where`的快捷方式，有`condition = ~(numpy.isfinite(arr))`。

> **语法:** `numpy.ma.masked_invalid(arr, copy=True)`
> 
> **参数:**
> **arr:**【ndarray】输入我们要屏蔽的数组。
> **复制:**【bool】如果为真(默认)，在结果中复制一份 arr。如果为假，就地修改 arr 并返回视图。
> 
> **返回:**【屏蔽数组】屏蔽后的结果数组。

**代码#1 :**

```py
# Python program explaining
# numpy.MaskedArray.masked_invalid() method 

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array with invalid values
in_arr = geek.array([1, 2, geek.nan, -1, geek.inf])
print ("Input array : ", in_arr)

# applying MaskedArray.masked_invalid  
# methods to input array 
mask_arr = ma.masked_invalid(in_arr)
print ("Masked array : ", mask_arr)
```

**Output:**

```py
Input array :  [ 1\.  2\. nan -1\. inf]
Masked array :  [1.0 2.0 -- -1.0 --]

```

**代码#2 :**

```py
# Python program explaining
# numpy.MaskedArray.masked_invalid() method 

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array with invalid element
in_arr = geek.array([5e8, 3e-5, geek.nan, 4e4, 5e2])
print ("Input array : ", in_arr)

# applying MaskedArray.masked_invalid  
# methods to input array 
mask_arr = ma.masked_invalid(in_arr)
print ("Masked array : ", mask_arr)
```

**Output:**

```py
Input array :  [5.e+08 3.e-05    nan 4.e+04 5.e+02]
Masked array :  [500000000.0 3e-05 -- 40000.0 500.0]

```
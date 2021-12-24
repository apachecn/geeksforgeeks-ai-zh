# Numpy maskearray . anom()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-anom-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-anom-function-python/)

在许多情况下，数据集可能是不完整的，或者被无效数据污染。例如，传感器可能未能记录数据，或者记录了无效值。`numpy.ma`模块通过引入屏蔽数组提供了一种解决这个问题的便捷方法。屏蔽数组是指可能缺少条目或条目无效的数组。

**`numpy.MaskedArray.anom()`** 函数计算沿给定轴的异常(与算术平均值的偏差)。它返回一个异常数组，形状与输入相同，算术平均值沿给定轴计算。

> **语法:** `numpy.MaskedArray.anom(axis=None, dtype=None)`
> 
> **参数:**
> **轴:**【int 或 None】异常所在的轴。
> **数据类型:**【数据类型，可选】用于计算方差的类型。
> 
> **返回:**【ndarray】一组异常。

**代码#1 :**

```
# Python program explaining
# numpy.MaskedArray.anom() method 

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array 
in_arr = geek.array([1, 2, 3, -1, 5])
print ("Input array : ", in_arr)

# Now we are creating a masked array
# by making third entry as invalid. 
mask_arr = ma.masked_array(in_arr, mask =[0, 0, 1, 0, 0])
print ("Masked array : ", mask_arr)

# applying MaskedArray.anom methods to mask array
out_arr = mask_arr.anom()
print ("Output anomalies array : ", out_arr)
```

**Output:**

```
Input array :  [ 1  2  3 -1  5]
Masked array :  [1 2 -- -1 5]
Output anomalies array :  [-0.75 0.25 -- -2.75 3.25]

```

**代码#2 :**

```
# Python program explaining
# numpy.MaskedArray.anom() method 

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array 
in_arr = geek.array([10, 20, 30, 40, 50])
print ("Input array : ", in_arr)

# Now we are creating a masked array by making 
# first and third entry as invalid. 
mask_arr = ma.masked_array(in_arr, mask =[1, 0, 1, 0, 0])
print ("Masked array : ", mask_arr)

# applying MaskedArray.anom methods to mask array
out_arr = mask_arr.anom()
print ("Output anomalies array : ", out_arr)
```

**Output:**

```
nput array :  [10 20 30 40 50]
Masked array :  [-- 20 -- 40 50]
Output anomalies array :  [-- -16.666666666666664 -- 3.3333333333333357 13.333333333333336]

```
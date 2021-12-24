# Numpy maskearray . swapaxes()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-swapaxes-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-swapaxes-function-python/)

**`numpy.MaskedArray.swapaxes()`** 功能用于返回 axis1 和 axis2 互换的屏蔽阵列视图。

> **语法:** `numpy.ma.swapaxes(axis1, axis2)`
> 
> **参数:**
> **轴 1:**【int】第一轴。
> **轴 2:**【int】第二轴。
> 
> **返回:**【交换 _ 数组】结果数组。

**代码#1 :**

```
# Python program explaining
# numpy.MaskedArray.swapaxes() method 

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

# creating input array  
in_arr = geek.array([[1, 2], [ 3, -1], [ 5, -3]])
print ("Input array : ", in_arr) 

# Now we are creating a masked array. 
# by making  entry as invalid.  
mask_arr = ma.masked_array(in_arr, mask =[[ 1, 0], [ 0, 1], [ 0, 0]]) 
print ("Masked array : ", mask_arr) 

# applying MaskedArray.swapaxes methods 
# to masked array 
out_arr = mask_arr.swapaxes(0, 1) 
print ("Output swapped masked array : ", out_arr) 
```

**Output:**

```
Input array :  [[ 1  2]
 [ 3 -1]
 [ 5 -3]]
Masked array :  [[-- 2]
 [3 --]
 [5 -3]]
Output swapped masked array :  [[-- 3 5]
 [2 -- -3]]

```

**代码#2 :**

```
# Python program explaining
# numpy.MaskedArray.swapaxes() method 

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

# creating input array 
in_arr = geek.array([[[ 2e8, 3e-5]], [[ -45.0, 2e5]]])
print ("Input array : ", in_arr)

# Now we are creating a masked array. 
# by making one entry as invalid.  
mask_arr = ma.masked_array(in_arr, mask =[[[ 1, 0]], [[ 0, 0]]]) 
print ("3D Masked array : ", mask_arr) 

# applying MaskedArray.swapaxes methods 
# to masked array
out_arr = mask_arr.swapaxes(0, 2) 
print ("Output swapped masked array : ", out_arr)
```

**Output:**

```
Input array :  [[[ 2.0e+08  3.0e-05]]

 [[-4.5e+01  2.0e+05]]]
3D Masked array :  [[[-- 3e-05]]

 [[-45.0 200000.0]]]
Output swapped masked array :  [[[-- -45.0]]

 [[3e-05 200000.0]]]

```
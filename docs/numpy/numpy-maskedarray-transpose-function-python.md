# Numpy maskearray .转置()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-transpose-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-transpose-function-python/)

**`numpy.MaskedArray.transpose()`** 函数用于置换被屏蔽数组的维度。

> **语法:** `numpy.ma.transpose(axis)`
> 
> **参数:**
> **轴:**【整数列表，可选】默认情况下，反转尺寸，否则根据给定值排列轴。
> 
> **返回:**【ndarray】轴已置换的结果数组..

**代码#1 :**

```
# Python program explaining
# numpy.MaskedArray.transpose() method 

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

# applying MaskedArray.transpose methods 
# to masked array 
out_arr = mask_arr.transpose() 
print ("Output transposed masked array : ", out_arr) 
```

**Output:**

```
Input array :  [[ 1  2]
 [ 3 -1]
 [ 5 -3]]
Masked array :  [[-- 2]
 [3 --]
 [5 -3]]
Output transposed masked array :  [[-- 3 5]

```

**代码#2 :**

```
# Python program explaining
# numpy.MaskedArray.transpose() method 

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

# applying MaskedArray.transpose methods 
# to masked array
out_arr = mask_arr.transpose() 
print ("Output transposed masked array : ", out_arr)
```

**Output:**

```
Input array :  [[[ 2.0e+08  3.0e-05]]

 [[-4.5e+01  2.0e+05]]]
3D Masked array :  [[[-- 3e-05]]

 [[-45.0 200000.0]]]
Output transposed masked array :  [[[-- -45.0]]

 [[3e-05 200000.0]]]

```
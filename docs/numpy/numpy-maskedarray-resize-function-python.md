# Numpy maskearray . resize()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-resize-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-resize-function-python/)

**`numpy.MaskedArray.resize()`** 函数用于从给定数组中创建一个具有指定大小和形状的新掩码数组。新数组填充了 arr 的重复副本(按照数据存储在内存中的顺序)。如果 arr 被屏蔽，新数组将被屏蔽，新掩码将是旧数组的重复。

> **语法:** `numpy.ma.resize(arr, new_shape)`
> 
> **参数:**
> **arr:** 要调整大小的输入数组。
> **new _ shape:**【int 或 int 元组】调整大小数组的新形状。
> 
> **返回:**【调整大小 _ 数组】数组的新形状。

**代码#1 :**

```py
# Python program explaining
# numpy.MaskedArray.resize() method 

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

# creating input array of 2 * 2  
in_arr = geek.array([[10, 20], [-10, 40]]) 
print ("Input array : ", in_arr) 

# Now we are creating a masked array. 
# by making one entry as invalid.  
mask_arr = ma.masked_array(in_arr, mask =[[ 1, 0], [ 0, 0]]) 
print ("Masked array : ", mask_arr) 

# applying MaskedArray.resize methods to make  
# it a 3 * 3 masked array
out_arr = ma.resize(mask_arr, (3, 3)) 
print ("Output resized masked array : ", out_arr) 
```

**Output:**

```py
Input array :  [[ 10  20]
 [-10  40]]
Masked array :  [[-- 20]
 [-10 40]]
Output resized masked array :  [[-- 20 -10]
 [40 -- 20]
 [-10 40 --]]

```

**代码#2 :**

```py
# Python program explaining
# numpy.MaskedArray.resize() method 

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

# creating input array 
in_arr = geek.array([[[ 2e8, 3e-5]], [[ -4e-6, 2e5]]])
print ("Input array : ", in_arr) 

# Now we are creating a masked array. 
# by making one entry as invalid.  
mask_arr = ma.masked_array(in_arr, mask =[[[ 1, 0]], [[ 0, 0]]]) 
print ("Masked array : ", mask_arr) 

# applying MaskedArray.resize methods to make  
# it a 1 * 6 masked array
out_arr = ma.resize(mask_arr, (1, 6)) 
print ("Output resized masked array : ", out_arr)  
```

**Output:**

```py
Input array :  [[[ 2.e+08  3.e-05]]

 [[-4.e-06  2.e+05]]]
Masked array :  [[[-- 3e-05]]

 [[-4e-06 200000.0]]]
Output resized masked array :  [[-- 3e-05 -4e-06 200000.0 -- 3e-05]]
?

```
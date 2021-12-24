# Numpy maskearray . resform()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-masked array-resform-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-reshape-function-python/)

**`numpy.MaskedArray.reshape()`** 功能用于在不改变其数据的情况下，给被屏蔽的数组赋予一个新的形状。它返回一个包含相同数据但具有新形状的屏蔽数组。结果是原始数组的视图；如果这不可能，则会引发 ValueError。

> **语法:** `numpy.ma.reshape(shape, order)`
> 
> **参数:**
> 
> **形状:**【int 或 int 的元组】新形状应该与原始形状兼容。
> **顺序:** ['C '，' F '，' A '，' K '，可选]默认使用' C '索引顺序。
> –>使用此索引顺序读取的元素。
> –>‘C’表示以类 C 顺序索引元素，最后一个轴索引变化最快，回到第一个轴索引变化最慢。
> –>“F”表示以类似 Fortran 的索引顺序对元素进行索引，第一个索引变化最快，最后一个索引变化最慢。
> –>“A”表示以类似 Fortran 的索引顺序读取元素，如果 m 在内存中是 Fortran 连续的，则以类似 C 的顺序读取。
> –>“K”表示按照元素在内存中出现的顺序读取元素，除了当步长为负时反转数据。
> 
> **返回:**【重塑 _ 数组】数组上的新视图。

**代码#1 :**

```
# Python program explaining
# numpy.MaskedArray.reshape() method 

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

# creating input array  
in_arr = geek.array([1, 2, 3, -1]) 
print ("Input array : ", in_arr) 

# Now we are creating a masked array. 
# by making third entry as invalid.  
mask_arr = ma.masked_array(in_arr, mask =[1, 0, 1, 0]) 
print ("Masked array : ", mask_arr) 

# applying MaskedArray.reshape methods to make  
# it a 2d masked array
out_arr = mask_arr.reshape(2, 2) 
print ("Output 2D masked array : ", out_arr) 
```

**Output:**

```
Input array :  [ 1  2  3 -1]
Masked array :  [-- 2 -- -1]
Output 2D masked array :  [[-- 2]
 [-- -1]]

```

**代码#2 :**

```
# Python program explaining
# numpy.MaskedArray.reshape() method 

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

# applying MaskedArray.reshape methods to make  
# it a 2d masked array
out_arr = mask_arr.reshape(1, 4) 
print ("Output 2D masked array : ", out_arr) 
print()

# applying MaskedArray.reshape methods to make  
# it a 1d masked array
out_arr = mask_arr.reshape(4, ) 
print ("Output 1D masked array : ", out_arr)  
```

**Output:**

```
Input array :  [[[ 2.0e+08  3.0e-05]]

 [[-4.5e+01  2.0e+05]]]
3D Masked array :  [[[-- 3e-05]]

 [[-45.0 200000.0]]]
Output 2D masked array :  [[-- 3e-05 -45.0 200000.0]]

Output 1D masked array :  [-- 3e-05 -45.0 200000.0]

```
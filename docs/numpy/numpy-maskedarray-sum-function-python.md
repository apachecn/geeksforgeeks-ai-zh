# Numpy maskearray . sum()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-sum-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-sum-function-python/)

**`numpy.MaskedArray.median()`** 函数用于计算给定轴上被屏蔽的数组元素的总和。

> **语法:** `numpy.ma.sum(arr, axis=None, dtype=None, out=None, keepdims=False)`
> 
> **参数:**
> 
> **arr:**【ndarray】输入屏蔽数组。
> **轴:**【int，可选】计算总和的轴。默认值(无)是计算展平数组的总和。
> **数据类型:**【数据类型，可选】返回数组的类型，以及元素相乘的累加器的类型。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> **保持尺寸:**【布尔，可选】如果设置为真，则缩小的轴作为尺寸为 1 的尺寸留在结果中。使用此选项，结果将根据输入数组正确广播。
> 
> **Return:**【sum _ along _ axis，ndarray】除非指定 out，否则将返回一个保存结果的新数组，在这种情况下，将返回对 out 的引用。

**代码#1 :**

```py
# Python program explaining
# numpy.MaskedArray.sum() method 

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

# creating input array  
in_arr = geek.array([[1, 2], [ 3, -1], [ 5, -3]])
print ("Input array : ", in_arr) 

# Now we are creating a masked array. 
# by making  entry as invalid.  
mask_arr = ma.masked_array(in_arr, mask =[[1, 0], [ 1, 0], [ 0, 0]]) 
print ("Masked array : ", mask_arr) 

# applying MaskedArray.sum    
# methods to masked array
out_arr = ma.sum(mask_arr) 
print ("sum of masked array along default axis : ", out_arr) 
```

**Output:**

```py
Input array :  [[ 1  2]
 [ 3 -1]
 [ 5 -3]]
Masked array :  [[-- 2]
 [-- -1]
 [5 -3]]
sum of masked array along default axis :  3

```

**代码#2 :**

```py
# Python program explaining
# numpy.MaskedArray.sum() method 

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

# creating input array 
in_arr = geek.array([[1, 0, 3], [ 4, 1, 6]]) 
print ("Input array : ", in_arr)

# Now we are creating a masked array. 
# by making one entry as invalid.  
mask_arr = ma.masked_array(in_arr, mask =[[ 0, 0, 0], [ 0, 0, 1]]) 
print ("Masked array : ", mask_arr) 

# applying MaskedArray.sum methods 
# to masked array
out_arr1 = ma.sum(mask_arr, axis = 0) 
print ("sum of masked array along 0 axis : ", out_arr1)

out_arr2 = ma.sum(mask_arr, axis = 1) 
print ("sum of masked array along 1 axis : ", out_arr2)
```

**Output:**

```py
Input array :  [[1 0 3]
 [4 1 6]]
Masked array :  [[1 0 3]
 [4 1 --]]
sum of masked array along 0 axis :  [5 1 3]
sum of masked array along 1 axis :  [4 5]

```
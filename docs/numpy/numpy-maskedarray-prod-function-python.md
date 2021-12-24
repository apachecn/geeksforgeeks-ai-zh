# Numpy maskearray . prod()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-prod-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-prod-function-python/)

**`numpy.MaskedArray.prod()`** 函数用于计算给定轴上数组元素的乘积。这里，屏蔽元素在内部设置为 1，用于计算。

> **语法:** `numpy.ma.prod(self, axis=None, dtype=None, out=None, keepdims=False)`
> 
> **参数:**
> 
> **arr:**【ndarray】输入屏蔽数组。
> **轴:**【int，可选】计算产品的轴。默认值(无)是在展平的数组上计算乘积。
> **数据类型:**【数据类型，可选】返回数组的类型，以及元素相乘的累加器的类型。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> **保持尺寸:**【布尔，可选】如果设置为真，则缩小的轴作为尺寸为 1 的尺寸留在结果中。使用此选项，结果将根据输入数组正确广播。
> 
> **返回:**【product _ 沿 _ 轴，ndarray】除非指定 out，否则将返回一个保存结果的新数组，在这种情况下，将返回对 out 的引用。

**代码#1 :**

```py
# Python program explaining
# numpy.MaskedArray.prod() method 

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

# applying MaskedArray.prod    
# methods to masked array
out_arr = ma.prod(mask_arr) 
print ("product of masked array along default axis : ", out_arr) 
```

**Output:**

```py
Input array :  [[ 1  2]
 [ 3 -1]
 [ 5 -3]]
Masked array :  [[-- 2]
 [-- -1]
 [5 -3]]
product of masked array along default axis :  30

```

**代码#2 :**

```py
# Python program explaining
# numpy.MaskedArray.prod() method 

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

# applying MaskedArray.prod methods 
# to masked array
out_arr1 = ma.prod(mask_arr, axis = 0) 
print ("product of masked array along 0 axis : ", out_arr1)

out_arr2 = ma.prod(mask_arr, axis = 1) 
print ("product of masked array along 1 axis : ", out_arr2)
```

**Output:**

```py
Input array :  [[1 0 3]

 [4 1 6]]

Masked array :  [[1 0 3]

 [4 1 --]]

product of masked array along 0 axis :  [4 0 3]

product of masked array along 1 axis :  [0 4]

```
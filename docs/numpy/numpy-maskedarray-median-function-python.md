# Numpy maskearray .中位数()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-median-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-median-function-python/)

**`numpy.MaskedArray.median()`** 函数用于计算沿指定轴的被屏蔽数组的中值。它返回数组元素的中值。

> **语法:** `numpy.ma.median(arr, axis=None, out=None, overwrite_input=False, keepdims=False)`
> 
> **参数:**
> 
> **arr:**【ndarray】输入屏蔽数组。
> **轴:**【int，可选】计算中间值的轴。默认值(无)是计算展平数组的中值。
> **数据类型:**【数据类型，可选】返回数组的类型，以及元素相乘的累加器的类型。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> **overwrite _ input:**【bool，可选】如果为 True，则允许使用输入数组的内存进行计算。对中值的调用将修改输入数组。当您不需要保留输入数组的内容时，这将节省内存。将输入视为未定义，但它可能会完全或部分排序。默认值为假。请注意，如果 overwrite_input 为 True，并且该输入还不是数组，则会引发错误。
> **保持尺寸:**【布尔，可选】如果设置为真，减少的轴将作为尺寸为 1 的尺寸留在结果中。使用此选项，结果将根据输入数组正确广播。
> 
> **Return :** 【中值 _ 沿 _ 轴，n 数组】除非指定 out，否则将返回一个保存结果的新数组，在这种情况下，将返回对 out 的引用。

**代码#1 :**

```py
# Python program explaining
# numpy.MaskedArray.median() method 

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

# applying MaskedArray.median    
# methods to masked array
out_arr = ma.median(mask_arr) 
print ("median of masked array along default axis : ", out_arr) 
```

**Output:**

```py
Input array :  [[ 1  2]
 [ 3 -1]
 [ 5 -3]]
Masked array :  [[-- 2]
 [-- -1]
 [5 -3]]
median of masked array along default axis :  0.5

```

**代码#2 :**

```py
# Python program explaining
# numpy.MaskedArray.median() method 

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

# applying MaskedArray.median methods 
# to masked array
out_arr1 = ma.median(mask_arr, axis = 0) 
print ("median of masked array along 0 axis : ", out_arr1)

out_arr2 = ma.median(mask_arr, axis = 1) 
print ("median of masked array along 1 axis : ", out_arr2)
```

**Output:**

```py
Input array :  [[1 0 3]
 [4 1 6]]
Masked array :  [[1 0 3]
 [4 1 --]]
median of masked array along 0 axis :  [2.5 0.5 3.0]
median of masked array along 1 axis :  [1.0 2.5]

```
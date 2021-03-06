# num py masked array . cumber()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-cum prod-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-cumprod-function-python/)

**`numpy.MaskedArray.cumprod()`** 返回给定轴上被屏蔽的数组元素的累积乘积。计算期间，屏蔽值在内部设置为 1。但是，它们的位置被保存，结果将在相同的位置被屏蔽。

> **语法:** `numpy.ma.cumprod(axis=None, dtype=None, out=None)`
> 
> **参数:**
> 
> **轴:**【int，可选】计算累计乘积的轴。缺省值(无)是计算展平数组上的积。
> **数据类型:**【数据类型，可选】返回数组的类型，以及元素相乘的累加器的类型。如果未指定 dtype，则默认为 arr 的 dtype，除非 arr 具有精度小于默认平台整数的整数 dtype。在这种情况下，将使用默认的平台整数。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> 
> **Return:**【cumprod _ along _ axis，ndarray】除非指定 out，否则将返回一个保存结果的新数组，在这种情况下，将返回对 out 的引用。

**代码#1 :**

```py
# Python program explaining
# numpy.MaskedArray.cumprod() method 

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

# applying MaskedArray.cumprod    
# methods to masked array
out_arr = mask_arr.cumprod() 
print ("cumulative product of masked array along default axis : ", out_arr)     
```

**Output:**

```py
Input array :  [[ 1  2]
 [ 3 -1]
 [ 5 -3]]
Masked array :  [[-- 2]
 [-- -1]
 [5 -3]]
cumulative sum of masked array along default axis :  [-- 2 -- -2 -10 30]

```

**代码#2 :**

```py
# Python program explaining
# numpy.MaskedArray.cumprod() method 

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

# applying MaskedArray.cumprod methods 
# to masked array
out_arr1 = mask_arr.cumprod(axis = 0) 
print ("cumulative product of masked array along 0 axis : ", out_arr1)

out_arr2 = mask_arr.cumprod(axis = 1) 
print ("cumulative product of masked array along 1 axis : ", out_arr2)
```

**Output:**

```py
Input array :  [[1 0 3]
 [4 1 6]]
Masked array :  [[1 0 3]
 [4 1 --]]
cumulative product of masked array along 0 axis :  [[1 0 3]
 [4 0 --]]
cumulative product of masked array along 1 axis :  [[1 0 0]
 [4 4 --]]

```
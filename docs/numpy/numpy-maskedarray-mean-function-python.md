# Numpy maskearray . mean()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-mean-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-mean-function-python/)

**`numpy.MaskedArray.mean()`** 函数用于返回沿给定轴的掩码数组元素的平均值。这里被屏蔽的条目被忽略，并且非有限的结果元素将被屏蔽。

> **语法:** `numpy.ma.mean(axis=None, dtype=None, out=None)`
> 
> **参数:**
> 
> **轴:**【int，可选】计算平均值的轴。默认值(无)是计算展平数组的平均值。
> **数据类型:**【数据类型，可选】返回数组的类型，以及元素相乘的累加器的类型。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> 
> **Return:**【mean _ along _ axis，ndarray】除非指定 out，否则将返回一个保存结果的新数组，在这种情况下，将返回对 out 的引用。

**代码#1 :**

```py
# Python program explaining
# numpy.MaskedArray.mean() method 

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

# applying MaskedArray.mean    
# methods to masked array
out_arr = mask_arr.mean() 
print ("mean of masked array along default axis : ", out_arr) 
```

**Output:**

```py
Input array :  [[ 1  2]
 [ 3 -1]
 [ 5 -3]]
Masked array :  [[-- 2]
 [-- -1]
 [5 -3]]
mean of masked array along default axis :  0.75

```

**代码#2 :**

```py
# Python program explaining
# numpy.MaskedArray.mean() method 

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

# applying MaskedArray.mean methods 
# to masked array
out_arr1 = mask_arr.mean(axis = 0) 
print ("mean of masked array along 0 axis : ", out_arr1)

out_arr2 = mask_arr.mean(axis = 1) 
print ("mean of masked array along 1 axis : ", out_arr2)
```

**Output:**

```py
Input array :  [[1 0 3]
 [4 1 6]]
Masked array :  [[1 0 3]
 [4 1 --]]
mean of masked array along 0 axis :  [2.5 0.5 3.0]
mean of masked array along 1 axis :  [1.3333333333333333 2.5]

```
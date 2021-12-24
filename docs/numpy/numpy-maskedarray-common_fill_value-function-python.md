# Numpy maskearray . common _ fill _ value()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-common _ fill _ value-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-common_fill_value-function-python/)

**`numpy.MaskedArray.common_fill_value()`** 函数用于返回两个掩码数组之间的公共填充值。如果`arr1.fill_value == arr2.fill_value`则返回填充值，否则返回无。

> **语法:** `numpy.ma.common_fill_value(arr1, arr2)`
> 
> **参数:**
> **arr1、arr2 :** 【掩码数组】要比较填充值的掩码数组。
> 
> **返回:**【标量或无】常用填充值或无。

**代码#1 :**

```py
# Python program explaining
# numpy.MaskedArray.common_fill_value() method 

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

# creating input arrays  
in_arr1 = geek.array([[1, 2], [ 3, -1], [ 5, -3]])
print ("1st Input array : ", in_arr1) 

in_arr2 = geek.array([[10, 20], [ 30, -10], [ 50, -30]])
print ("2nd Input array : ", in_arr2) 

# Now we are creating masked arrays. 
# by making  entry as invalid.  
mask_arr1 = ma.masked_array(in_arr1, mask =[[1, 0], [ 1, 0], [ 0, 0]],
                                                       fill_value = 5) 
print ("1st Masked array : ", mask_arr1) 

mask_arr2 = ma.masked_array(in_arr2, mask =[[1, 1], [ 1, 0], [ 0, 0]], 
                                                      fill_value = 5) 
print ("2nd Masked array : ", mask_arr2) 

# applying MaskedArray.common_fill_value    
# methods to masked array
out_arr = ma.common_fill_value(mask_arr1, mask_arr2) 
print ("common filled value : ", out_arr) 
```

**Output:**

```py
1st Input array :  [[ 1  2]
 [ 3 -1]
 [ 5 -3]]
2nd Input array :  [[ 10  20]
 [ 30 -10]
 [ 50 -30]]
1st Masked array :  [[-- 2]
 [-- -1]
 [5 -3]]
2nd Masked array :  [[-- --]
 [-- -10]
 [50 -30]]
common filled value :  5

```

**代码#2 :**

```py
# Python program explaining
# numpy.MaskedArray.common_fill_value() method 

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

# creating input arrays  
in_arr1 = geek.array([[1, 2], [ 3, -1], [ 5, -3]])
print ("1st Input array : ", in_arr1) 

in_arr2 = geek.array([[10, 20], [ 30, -10], [ 50, -30]])
print ("2nd Input array : ", in_arr2) 

# Now we are creating masked arrays. 
# by making  entry as invalid.  
mask_arr1 = ma.masked_array(in_arr1, mask =[[1, 0], [ 1, 0], [ 0, 0]],
                                                      fill_value = 5) 
print ("1st Masked array : ", mask_arr1) 

mask_arr2 = ma.masked_array(in_arr2, mask =[[1, 1], [ 1, 0], [ 0, 0]],
                                                     fill_value = 10) 
print ("2nd Masked array : ", mask_arr2) 

# applying MaskedArray.common_fill_value    
# methods to masked array
out_arr = ma.common_fill_value(mask_arr1, mask_arr2) 
print ("common filled value : ", out_arr) 
```

**Output:**

```py
1st Input array :  [[ 1  2]
 [ 3 -1]
 [ 5 -3]]
2nd Input array :  [[ 10  20]
 [ 30 -10]
 [ 50 -30]]
1st Masked array :  [[-- 2]
 [-- -1]
 [5 -3]]
2nd Masked array :  [[-- --]
 [-- -10]
 [50 -30]]
common filled value :  None

```
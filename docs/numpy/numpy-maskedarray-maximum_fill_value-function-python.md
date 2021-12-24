# Numpy maskearray . maximum _ fill _ value()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-masked array-maximum _ fill _ value-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-maximum_fill_value-function-python/)

**`numpy.MaskedArray.maximum_fill_value()`** 函数用于返回一个对象的数据类型所能表示的最小值。

> **语法:** `numpy.ma.maximum_fill_value(obj)`
> 
> **参数:**
> **对象:**【n 数组、数据类型或标量】返回最小填充值的数组数据类型或标量。
> 
> **返回:**【标量】最小填充值。

**代码#1 :**

```
# Python program explaining
# numpy.MaskedArray.maximum_fill_value() method 

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

# creating input array  
in_arr = geek.array([1,  3,  5, -3], dtype ='float')
print ("Input array : ", in_arr) 

# Now we are creating a masked array. 
# by making  entry as invalid.  
mask_arr = ma.masked_array(in_arr, mask =[1, 0, 0, 0]) 
print ("Masked array : ", mask_arr) 

# applying MaskedArray.maximum_fill_value    
# methods to masked array
out_val = ma.maximum_fill_value(mask_arr) 
print ("Minimum filled value : ", out_val) 
```

**Output:**

```
Input array :  [ 1\.  3\.  5\. -3.]
Masked array :  [-- 3.0 5.0 -3.0]
Minimum filled value :  -inf

```

**代码#2 :**

```
# Python program explaining
# numpy.MaskedArray.maximum_fill_value() method 

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

# applying MaskedArray.maximum_fill_value    
# methods to masked array
out_val = ma.maximum_fill_value(mask_arr) 
print ("Minimum filled value : ", out_val)  
```

**Output:**

```
Input array :  [[ 1  2]
 [ 3 -1]
 [ 5 -3]]
Masked array :  [[-- 2]
 [-- -1]
 [5 -3]]
Minimum filled value :  -2147483648

```
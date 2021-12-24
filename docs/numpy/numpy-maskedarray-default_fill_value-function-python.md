# Numpy maskedarray . default _ fill _ value()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-masked array-default _ fill _ value-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-default_fill_value-function-python/)

**`numpy.MaskedArray.default_fill_value()`** 函数用于返回参数对象的默认填充值。默认填充值取决于输入数组的数据类型或输入标量的类型。如果数据类型是 bool，那么缺省填充值是 True，对于 int 是 999999，对于 float 是 1.e20，对于 complex 是 1.e20+0.j，'？'对象为，字符串为“不适用”。

> **语法:** `numpy.ma.default_fill_value(obj)`
> 
> **参数:**
> **对象:**【n 数组、数据类型或标量】返回默认填充值的数组数据类型或标量。
> 
> **返回:**【标量】默认填充值。

**代码#1 :**

```py
# Python program explaining
# numpy.MaskedArray.default_fill_value() method 

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

# creating input array  
in_arr = geek.array([[1, 2], [ 3, -1], [ 5, -3]])
print ("Input array : ", in_arr) 

# Now we are creating a masked array. 
# by making  entry as invalid.  
mask_arr = ma.masked_array(in_arr,
     mask =[[1, 0], [ 1, 0], [ 0, 0]]) 

print ("Masked array : ", mask_arr) 

# applying MaskedArray.default_fill_value    
# methods to masked array
out_val = ma.default_fill_value(mask_arr) 
print ("Default filled value : ", out_val) 
```

**Output:**

```py
Input array :  [[ 1  2]
 [ 3 -1]
 [ 5 -3]]
Masked array :  [[-- 2]
 [-- -1]
 [5 -3]]
Default filled value :  999999

```

**代码#2 :**

```py
# Python program explaining
# numpy.MaskedArray.default_fill_value() method 

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

# creating input array  
in_arr = geek.array([[1 + 2j, 2 + 3j],
                     [ 3-2j, -1 + 2j],
                     [ 5-4j, -3-3j]])
print ("Input array : ", in_arr) 

# Now we are creating a masked array. 
# by making two entry as invalid.  
mask_arr = ma.masked_array(in_arr, 
     mask =[[1, 0], [ 1, 0], [ 0, 0]]) 

print ("Masked array : ", mask_arr) 

# applying MaskedArray.default_fill_value    
# methods to masked array
out_val = ma.default_fill_value(mask_arr) 
print ("Default filled value : ", out_val) 
```

**Output:**

```py
Input array :  [[ 1.+2.j  2.+3.j]
 [ 3.-2.j -1.+2.j]
 [ 5.-4.j -3.-3.j]]
Masked array :  [[-- (2+3j)]
 [-- (-1+2j)]
 [(5-4j) (-3-3j)]]
Default filled value :  (1e+20+0j)

```
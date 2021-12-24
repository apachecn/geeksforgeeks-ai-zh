# Numpy maskearray .至少 _3d()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-masked array-至少 _3d-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-atleast_3d-function-python/)

**`numpy.MaskedArray.atleast_3d()`** 函数用于将输入转换为至少三维的屏蔽数组。标量、一维和二维数组被转换为三维数组，而高维输入被保留。

> **语法:** `numpy.ma.atleast_3d(*arys)`
> 
> **参数:**
> **arys:**【array _ like】一个或多个输入数组。
> 
> **返回:**一个数组或数组列表，每个数组都有`arr.ndim >= 3`

**代码#1 :**

```py
# Python program explaining
# numpy.MaskedArray.atleast_3d() method 

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

# creating input arrays  
in_arr1 = geek.array([ 3, -1, 5, -3])
print ("1st Input array : ", in_arr1)

in_arr2 = geek.array(2)
print ("2nd Input array : ", in_arr2)

in_arr3 = geek.array([[1, 2], [ 3, -1], [ 5, -3]])
print ("3rd Input array : ", in_arr3) 

# Now we are creating  masked array. 
# by making  entry as invalid.  
mask_arr1 = ma.masked_array(in_arr1, mask =[ 1, 0, 1, 0]) 
print ("1st Masked array : ", mask_arr1)

mask_arr2 = ma.masked_array(in_arr2, mask = 0) 
print ("2nd Masked array : ", mask_arr2)

mask_arr3 = ma.masked_array(in_arr3, mask =[[ 1, 0], [ 0, 1], [ 0, 0]]) 
print ("3rd Masked array : ", mask_arr3)

# applying MaskedArray.atleast_3d methods 
# to masked array 
out_arr = ma.atleast_2d(mask_arr1, mask_arr2, mask_arr3) 
print ("Output masked array : ", out_arr) 
```

**Output:**

```py
1st Input array :  [ 3 -1  5 -3]
2nd Input array :  2
3rd Input array :  [[ 1  2]
 [ 3 -1]
 [ 5 -3]]
1st Masked array :  [-- -1 -- -3]
2nd Masked array :  2
3rd Masked array :  [[-- 2]
 [3 --]
 [5 -3]]
Output masked array :  [masked_array(data=[[--, -1, --, -3]],
             mask=[[ True, False,  True, False]],
       fill_value=999999), masked_array(data=[[2]],
             mask=[[False]],
       fill_value=999999), masked_array(
  data=[[--, 2],
        [3, --],
        [5, -3]],
  mask=[[ True, False],
        [False,  True],
        [False, False]],
  fill_value=999999)]

```

**代码#2 :**

```py
# Python program explaining
# numpy.MaskedArray.atleast_3d() method 

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

# applying MaskedArray.atleast_3d methods 
# to masked array
out_arr = ma.atleast_3d(mask_arr) 
print ("Output masked array : ", out_arr)
```

**Output:**

```py
Input array :  [[[ 2.0e+08  3.0e-05]]

 [[-4.5e+01  2.0e+05]]]
3D Masked array :  [[[-- 3e-05]]

 [[-45.0 200000.0]]]
Output masked array :  [[[-- 3e-05]]

 [[-45.0 200000.0]]]

```
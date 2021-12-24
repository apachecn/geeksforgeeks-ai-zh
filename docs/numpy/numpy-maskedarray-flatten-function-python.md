# Numpy maskearray . flat()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-flat-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-flatten-function-python/)

**`numpy.MaskedArray.flatten()`** 功能是用来返回一个输入蒙版数组折叠成一维的副本。

> **语法:** `numpy.ma.flatten(order='C')`
> 
> **参数:**
> **顺序:**【‘C’，‘F’，‘A’，‘K’，可选】是按 C(行-主)、Fortran(列-主)顺序展平，还是保留 C/Fortran 从 A 开始排序，默认为‘C’。
> 
> **返回:**【n 数组】输入数组的副本，展平到一维。

**代码#1 :**

```
# Python program explaining
# numpy.MaskedArray.flatten() method 

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

# creating input array of 2 * 2  
in_arr = geek.array([[10, 20], [-10, 40]]) 
print ("Input array : ", in_arr) 

# Now we are creating a masked array 
# by making one entry as invalid.  
mask_arr = ma.masked_array(in_arr, mask =[[ 1, 0], [ 0, 0]]) 
print ("Masked array : ", mask_arr) 

# applying MaskedArray.flatten methods to make  
# it a 1D flattened array
out_arr = mask_arr.flatten() 
print ("Output flattened masked array : ", out_arr) 
```

**Output:**

```
Input array :  [[ 10  20]
 [-10  40]]
Masked array :  [[-- 20]
 [-10 40]]
Output flattened masked array :  [-- 20 -10 40]

```

**代码#2 :**

```
# Python program explaining
# numpy.MaskedArray.flatten() method 

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

# creating input array 
in_arr = geek.array([[[ 2e8, 3e-5]], [[ -4e-6, 2e5]]])
print ("Input array : ", in_arr) 

# Now we are creating a masked array 
# by making one entry as invalid.  
mask_arr = ma.masked_array(in_arr, mask =[[[ 1, 0]], [[ 0, 0]]]) 
print ("Masked array : ", mask_arr) 

# applying MaskedArray.flatten methods to make  
# it a 1D masked array
out_arr = mask_arr.flatten(order ='F') 
print ("Output flattened masked array : ", out_arr)
```

**Output:**

```
Input array :  [[[ 2.e+08  3.e-05]]

 [[-4.e-06  2.e+05]]]
Masked array :  [[[-- 3e-05]]

 [[-4e-06 200000.0]]]
Output flattened masked array :  [-- -4e-06 3e-05 200000.0]

```
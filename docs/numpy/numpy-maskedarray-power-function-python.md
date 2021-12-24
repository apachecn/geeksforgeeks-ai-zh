# Numpy maskearray . power()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-power-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-power-function-python/)

**`numpy.MaskedArray.power()`** 函数用于计算从第二个数组提升到幂的元素基数组。它将 arr1 中的每个基数提升到 arr2 中位置对应的幂。arr1 和 arr2 必须可宽铸为相同的形状。请注意，整数类型提升为负整数幂将会提升`ValueError`。

> **语法:** `numpy.ma.power(arr1, arr2, third=None)`
> 
> **参数:**
> **arr1 :** 【阵 _ 象】基地蒙面阵。
> **arr2 :** 【阵样】诸子掩阵。
> **第三个:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> 
> **返回:**【ndarray】arr 1 中的基数上升到 arr2 中的指数。

**代码#1 :**

```
# Python program explaining
# numpy.MaskedArray.power() method 

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

# creating base array 
base_arr = geek.array([0, 1, 2, 3, 4, 5]) 
print ("Input base array : ", base_arr)

# Now we are creating a base masked array. 
# by making one entry as invalid.  
base_mask_arr = ma.masked_array(base_arr, mask =[ 0, 0, 0, 0, 1, 0]) 
print ("Base Masked array : ", base_mask_arr) 

# creating exponent array 
exp_arr = geek.array([0, 2, 1, 4, 2, 3]) 
print ("Input exponent array : ", exp_arr)

# Now we are creating a exponent masked array. 
# by making one entry as invalid.  
exp_mask_arr = ma.masked_array(exp_arr, mask =[ 0, 1, 0, 0, 1, 0]) 
print ("Exponent Masked array : ", exp_mask_arr) 

# applying MaskedArray.power methods 
# to masked array
out_arr = ma.power(base_mask_arr, exp_mask_arr) 
print ("Output masked array : ", out_arr)
```

**Output:**

```
Input base array :  [0 1 2 3 4 5]

Base Masked array :  [0 1 2 3 -- 5]

Input exponent array :  [0 2 1 4 2 3]

Exponent Masked array :  [0 -- 1 4 -- 3]

Output masked array :  [1 -- 2 81 -- 125]

```
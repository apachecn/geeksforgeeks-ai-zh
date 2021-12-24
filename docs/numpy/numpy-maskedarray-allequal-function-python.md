# Numpy maskearray . allequal()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-allequal-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-allequal-function-python/)

在许多情况下，数据集可能是不完整的，或者被无效数据污染。例如，传感器可能未能记录数据，或者记录了无效值。`numpy.ma`模块通过引入屏蔽数组提供了一种解决这个问题的便捷方法。屏蔽数组是指可能缺少条目或条目无效的数组。

**`numpy.MaskedArray.allequal()`** 如果 a 和 b 的所有条目都相等，函数返回真，使用 fill_value 作为真值，其中一个或两个都被屏蔽。

> **语法:** `numpy.ma.allequal(arr1, arr2, fill_value=True)`
> 
> **参数:**
> **arr1、arr 2:**【array _ like】输入数组进行比较。
> **fill _ value:**【bool，可选】arr1 或 arr2 中的屏蔽值是否被视为相等(真)或不相等(假)。
> 
> **返回:**【bool】如果两个数组在给定容差内相等，则返回真，否则返回假。如果任一数组包含 NaN，则返回 False。

**代码#1 :**

```
# Python program explaining
# numpy.MaskedArray.allequal() method 

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating 1st input array 
in_arr1 = geek.array([1e8, 1e-5, -15.0])
print ("1st Input array : ", in_arr1)

# Now we are creating 1st masked array by making third entry as invalid. 
mask_arr1 = ma.masked_array(in_arr1, mask =[0, 0, 1])
print ("1st Masked array : ", mask_arr1)

# creating 2nd input array 
in_arr2 = geek.array([1e8, 1e-5, 15.0])
print ("2nd Input array : ", in_arr2)

# Now we are creating 2nd masked array by making third entry as invalid. 
mask_arr2 = ma.masked_array(in_arr2, mask =[0, 0, 1])
print ("2nd Masked array : ", mask_arr2)

# applying MaskedArray.allequal method
out_arr = ma.allequal(mask_arr1, mask_arr2, fill_value = False)
print ("Output array : ", out_arr)
```

**Output:**

```
1st Input array :  [ 1.0e+08  1.0e-05 -1.5e+01]
1st Masked array :  [100000000.0 1e-05 --]
2nd Input array :  [1.0e+08 1.0e-05 1.5e+01]
2nd Masked array :  [100000000.0 1e-05 --]
Output array :  False

```

**代码#2 :**

```
# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating 1st input array 
in_arr1 = geek.array([2e8, 3e-5, -45.0])
print ("1st Input array : ", in_arr1)

# Now we are creating 1st masked array by making third entry as invalid. 
mask_arr1 = ma.masked_array(in_arr1, mask =[0, 0, 1])
print ("1st Masked array : ", mask_arr1)

# creating 2nd input array 
in_arr2 = geek.array([2e8, 3e-5, 15.0])
print ("2nd Input array : ", in_arr2)

# Now we are creating 2nd masked array by making third entry as invalid. 
mask_arr2 = ma.masked_array(in_arr2, mask =[0, 0, 1])
print ("2nd Masked array : ", mask_arr2)
# applying MaskedArray.allequal method
out_arr = ma.allequal(mask_arr1, mask_arr2, fill_value = True)
print ("Output  array : ", out_arr)
```

**Output:**

```
1st Input array :  [ 2.0e+08  3.0e-05 -4.5e+01]
1st Masked array :  [200000000.0 3e-05 --]
2nd Input array :  [2.0e+08 3.0e-05 1.5e+01]
2nd Masked array :  [200000000.0 3e-05 --]
Output  array :  True

```
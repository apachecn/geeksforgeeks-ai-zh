# Numpy maskearray . all()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-masked array-all-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-all-function-python/)

在许多情况下，数据集可能是不完整的，或者被无效数据污染。例如，传感器可能未能记录数据，或者记录了无效值。`numpy.ma`模块通过引入屏蔽数组提供了一种解决这个问题的便捷方法。屏蔽数组是指可能缺少条目或条目无效的数组。

**`numpy.MaskedArray.all()`** 函数如果所有元素的计算结果都为真，则返回真。

> **语法:** `MaskedArray.all(axis=None, out=None, keepdims)`
> 
> **参数:**
> **轴:**【int 或 None】轴或执行逻辑与归约的轴。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> **保持尺寸:**【布尔，可选】如果设置为真，则缩小的轴作为尺寸为 1 的尺寸留在结果中。使用此选项，结果将根据输入数组正确广播。
> 
> **Return:**【ndarray，bool】除非指定 out，否则将返回新的布尔值或数组，在这种情况下，将返回对 out 的引用。

**代码#1 :**

```
# Python program explaining
# numpy.MaskedArray.all() method 

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array 
in_arr = geek.array([1, 2, 3, -1, 5])
print ("Input array : ", in_arr)

# applying MaskedArray.all methods to input array
out_arr = in_arr.all()
print ("Output array : ", out_arr)

# Now we are creating a masked array by 
# making third entry as invalid. 
mask_arr = ma.masked_array(in_arr, mask =[0, 0, 1, 0, 0])
print ("Masked array : ", mask_arr)

# applying MaskedArray.all methods to mask array
out_arr = mask_arr.all()
print ("Output array : ", out_arr)
```

**Output:**

```
Input array :  [ 1  2  3 -1  5]
Output array :  True
Masked array :  [1 2 -- -1 5]
Output array :  True

```

**代码#2 :**

```
# Python program explaining
# numpy.MaskedArray.all() method 

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array 
in_arr = geek.array([1, 2, 3, -1, 5])
print ("Input array : ", in_arr)

# Now we are creating a masked array by 
# making all entry as invalid. 
mask_arr = ma.masked_array(in_arr, mask =[1, 1, 1, 1, 1])
print ("Masked array : ", mask_arr)

# applying MaskedArray.all methods to mask array
out_arr = mask_arr.all()
print ("Output array : ", out_arr)
```

**Output:**

```
Input array :  [ 1  2  3 -1  5]
Masked array :  [-- -- -- -- --]
Output array :  --

```
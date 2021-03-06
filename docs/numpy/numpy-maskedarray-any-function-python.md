# Numpy maskearray . any()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-any-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-any-function-python/)

在许多情况下，数据集可能是不完整的，或者被无效数据污染。例如，传感器可能未能记录数据，或者记录了无效值。`numpy.ma`模块通过引入屏蔽数组提供了一种解决这个问题的便捷方法。屏蔽数组是指可能缺少条目或条目无效的数组。

**`numpy.MaskedArray.any()`** 函数的作用是:如果被屏蔽的数组中有任何元素的值为真，则返回真。在计算过程中，屏蔽值被视为假。

> **语法:** `numpy.MaskedArray.any(axis=None, out=None, keepdims)`
> 
> **参数:**
> **轴:**【无或整数或整数元组，可选】执行逻辑与归约的一个或多个轴。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> **保持尺寸:**【布尔，可选】如果设置为真，则缩小的轴作为尺寸为 1 的尺寸留在结果中。使用此选项，结果将根据输入数组正确广播。
> 
> **Return:**【bool 或 ndarray】除非指定 out，否则将返回新的 boolean 或 ndarray，在这种情况下，将返回对 out 的引用。

**代码#1 :**

```py
# Python program explaining
# numpy.MaskedArray.any() method 

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array 
in_arr = geek.array([1, 2, 3, -1, 5])
print ("Input array : ", in_arr)

# Now we are creating a masked array
# by making third entry as invalid. 
mask_arr = ma.masked_array(in_arr, mask =[0, 0, 1, 0, 0])
print ("Masked array : ", mask_arr)

# applying MaskedArray.anom methods to mask array
out_arr = mask_arr.anom()
print ("Output anomalies array : ", out_arr)
```

**Output:**

```py
Input array :  [ 1  2  3 -1  5]
Masked array :  [1 2 -- -1 5]
Output  array :  True

```

**代码#2 :**

```py
# Python program explaining
# numpy.MaskedArray.any() method 

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array 

in_arr = geek.array([1, 20, 30, 40, 50])
print ("Input array : ", in_arr)

# Now we are creating a masked array by making 
# all entry as invalid. 
mask_arr = ma.masked_array(in_arr, mask ='True')
print ("Masked array : ", mask_arr)

# applying MaskedArray.any methods to mask array
out_arr = mask_arr.any()
print ("Output array : ", out_arr)
```

**Output:**

```py
Input array :  [ 1 20 30 40 50]
Masked array :  [-- -- -- -- --]
Output array :  --

```
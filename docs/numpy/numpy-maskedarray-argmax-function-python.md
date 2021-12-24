# Numpy MaskedArray.argmax()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-arg max-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-argmax-function-python/)

在许多情况下，数据集可能是不完整的，或者被无效数据污染。例如，传感器可能未能记录数据，或者记录了无效值。`numpy.ma`模块通过引入屏蔽数组提供了一种解决这个问题的便捷方法。屏蔽数组是指可能缺少条目或条目无效的数组。

**`numpy.MaskedArray.argmax()`** 函数返回沿给定轴的最大值的指数数组。屏蔽值被视为具有值 fill_value..

> **语法:** `numpy.MaskedArray.argmax(axis=None, fill_value=None, out=None)`
> 
> **参数:**
> **轴:**【无，整数】如果无，则索引进入展平数组，否则沿指定轴。
> **fill _ Value:**【var，可选】用于填充屏蔽值的值。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> 
> **Return:**【index _ array】除非指定 out，否则将返回一个新的 integer_array，在这种情况下，将返回对 out 的引用。

**代码#1 :**

```
# Python program explaining
# numpy.MaskedArray.argmax() method 

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array 
in_arr = geek.array([1, 2, 3, -1, 5])
print ("Input array : ", in_arr)

# Now we are creating a masked array.
# by making third entry as invalid. 
mask_arr = ma.masked_array(in_arr, mask =[0, 0, 1, 0, 0])
print ("Masked array : ", mask_arr)

# applying MaskedArray.argmax methods to mask array
out_arr = mask_arr.argmax()
print ("Index of max element in masked array : ", out_arr)
```

**Output:**

```
Input array :  [ 1  2  3 -1  5]
Masked array :  [1 2 -- -1 5]
Index of max element in masked array :  4

```

**代码#2 :**

```
# Python program explaining
# numpy.MaskedArray.argmax() method 

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array 
in_arr = geek.array([10, 20, 30, -10, 50])
print ("Input array : ", in_arr)

# Now we are creating a masked array
# by making first third entry as invalid. 
mask_arr = ma.masked_array(in_arr, mask =[1, 0, 1, 0, 0])
print ("Masked array : ", mask_arr)

# applying MaskedArray.argmax methods to mask array
# and filling the masked location by 100
out_arr = mask_arr.argmax(fill_value = 100)
print ("Index of max element in masked array : ", out_arr)
```

**Output:**

```
Input array :  [ 10  20  30 -10  50]
Masked array :  [-- 20 -- -10 50]
Index of max element in masked array :  0

```
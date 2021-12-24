# Numpy maskearray . astype()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-as type-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-astype-function-python/)

在许多情况下，数据集可能是不完整的，或者被无效数据污染。例如，传感器可能未能记录数据，或者记录了无效值。numpy.ma 模块通过引入屏蔽阵列，提供了一种解决此问题的便捷方法。屏蔽数组是指可能缺少条目或条目无效的数组。
**numpy。函数的作用是:返回给定 newtype 的 MaskedArray 转换副本。** 

> **语法:** numpy。maskearray . astype(new Type)
> **参数:**
> **newtype :** 我们要转换被屏蔽数组的类型。
> **返回:**【maskedArray】一个自身施法的副本来输入 newtype。返回的记录形状与 self.shape 匹配。

**代码#1 :**

## 蟒蛇 3

```
# Python program explaining
# numpy.MaskedArray.astype() method

# importing numpy as geek
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array
in_arr = geek.array([1, 2, 3, -1, 5])
print ("Input array : ", in_arr)

# Now we are creating a masked array of int32
# and making third entry as invalid.
mask_arr = ma.masked_array(in_arr, mask =[0, 0, 1, 0, 0])
print ("Masked array : ", mask_arr)

# printing the data type of masked array
print(mask_arr.dtype)

# applying MaskedArray.astype methods to mask array
# and converting it to float64
out_arr = mask_arr.astype('float64')
print ("Output typecasted array : ", out_arr)

# printing the data type of typecasted masked array
print(out_arr.dtype)
```

**Output:** 

```
Input array :  [ 1  2  3 -1  5]
Masked array :  [1 2 -- -1 5]
int32
Output typecasted array :  [1.0 2.0 -- -1.0 5.0]
float64
```

**代码#2 :**

## 蟒蛇 3

```
# Python program explaining
# numpy.MaskedArray.astype() method

# importing numpy as geek
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array
in_arr = geek.array([10.1, 20.2, 30.3, 40.4, 50.5], dtype ='float64')
print ("Input array : ", in_arr)

# Now we are creating a masked array by making
# first and third entry as invalid.
mask_arr = ma.masked_array(in_arr, mask =[1, 0, 1, 0, 0])
print ("Masked array : ", mask_arr)

# printing the data type of masked array
print(mask_arr.dtype)

# applying MaskedArray.astype methods to mask array
# and converting it to int32
out_arr = mask_arr.astype('int32')
print ("Output typecasted array : ", out_arr)

# printing the data type of typecasted masked array
print(out_arr.dtype)
```

**Output:** 

```
Input array :  [10.1 20.2 30.3 40.4 50.5]
Masked array :  [-- 20.2 -- 40.4 50.5]
float64
Output typecasted array :  [-- 20 -- 40 50]
int32
```
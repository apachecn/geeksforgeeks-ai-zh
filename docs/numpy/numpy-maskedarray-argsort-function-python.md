# Numpy MaskedArray.argsort()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-arg sort-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-argsort-function-python/)

在许多情况下，数据集可能是不完整的，或者被无效数据污染。例如，传感器可能未能记录数据，或者记录了无效值。`numpy.ma`模块通过引入屏蔽数组提供了一种解决这个问题的便捷方法。屏蔽数组是指可能缺少条目或条目无效的数组。
**`numpy.MaskedArray.argsort()`** 函数返回一系列沿指定轴对数组进行排序的索引。屏蔽值会预先填充到 fill_value 中。

> **语法:** `numpy.MaskedArray.argsort(axis=None, kind='quicksort', order=None, endwith=True, fill_value=None)`
> 
> **参数:**
> **轴:**【无，整数】要排序的轴。如果默认值为“无”，则使用展平数组。
> **种类:** ['quicksort '，' mergesort '，' heapsort']排序算法。默认值为“快速排序”。
> **顺序:**【列表，可选】当 a 是定义了字段的数组时，此参数指定首先比较哪些字段，其次比较哪些字段等。
> **end with:**【True，False，可选】缺失值(如果有)应被视为最大值(True)还是最小值(False)当数组在数据类型的相同极端包含未屏蔽值时，这些值和屏蔽值的顺序是未定义的。
> **fill _ Value:**【var，可选】用于填充屏蔽值的值。如果无，最小填充值的输出(自。_data)来代替。
> 
> **返回:**【n 数组，int】沿指定轴排序的索引数组。

**代码#1 :**

```py
# Python program explaining
# numpy.MaskedArray.argsort() method 

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array 
in_arr = geek.array([4, 2, 3, -1, 5])
print ("Input array : ", in_arr)

# Now we are creating a masked array 
# by making third entry as invalid. 
mask_arr = ma.masked_array(in_arr, mask =[0, 0, 1, 0, 0])
print ("Masked array : ", mask_arr)

# applying MaskedArray.argsort methods to mask array
out_arr = mask_arr.argsort()
print ("output array of indices: ", out_arr)
```

**Output:**

```py
Input array :  [ 4  2  3 -1  5]
Masked array :  [4 2 -- -1 5]
output array of indices:  [3 1 0 4 2]

```

**代码#2 :**

```py
# Python program explaining
# numpy.MaskedArray.argsort() method 

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array 
in_arr = geek.array([5, -5, 0, -10, 2])
print ("Input array : ", in_arr)

# Now we are creating a masked array 
# by making first third entry as invalid. 
mask_arr = ma.masked_array(in_arr, mask =[1, 0, 1, 0, 0])
print ("Masked array : ", mask_arr)

# applying MaskedArray.argminmethods to mask array
# and filling the masked location by 1
out_arr = mask_arr.argsort(fill_value = 1)
print ("output array of indices: ", out_arr)
```

**Output:**

```py
Input array :  [  5  -5   0 -10   2]
Masked array :  [-- -5 -- -10 2]
output array of indices:  [3 1 0 2 4]

```
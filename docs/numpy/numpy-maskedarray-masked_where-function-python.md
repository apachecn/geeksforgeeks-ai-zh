# Numpy maskedarray . masked _ where()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-masked _ where-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-masked_where-function-python/)

在许多情况下，数据集可能是不完整的，或者被无效数据污染。例如，传感器可能未能记录数据，或者记录了无效值。`numpy.ma`模块通过引入屏蔽数组提供了一种解决这个问题的便捷方法。屏蔽数组是指可能缺少条目或条目无效的数组。

**`numpy.MaskedArray.masked_where()`** 函数用于屏蔽满足条件的数组。它以数组形式返回 arr，该数组在条件为真时被屏蔽。arr 或条件的任何屏蔽值也会在输出中被屏蔽。

> **语法:** `numpy.ma.masked_where(condition, arr, copy=True)`
> 
> **参数:**
> **条件:**【阵 _ 象】掩蔽条件。当条件测试浮点值是否相等时，请考虑改用 masked_values。
> **arr:**【ndarray】我们要屏蔽的输入数组。
> **复制:**【bool】如果为真(默认)，在结果中复制一份 arr。如果为假，就地修改 arr 并返回视图。
> 
> **返回:**【屏蔽数组】条件为真时屏蔽数组的结果..

**代码#1 :**

```
# Python program explaining
# numpy.MaskedArray.masked_where() method 

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array 
in_arr = geek.array([1, 2, 3, -1, 2])
print ("Input array : ", in_arr)

# applying MaskedArray.masked_where methods 
# to input array where value<= 1
mask_arr = ma.masked_where(in_arr<= 1, in_arr)
print ("Masked array : ", mask_arr)
```

**Output:**

```
Input array :  [ 1  2  3 -1  2]
Masked array :  [-- 2 3 -- 2]

```

**代码#2 :**

```
# Python program explaining
# numpy.MaskedArray.masked_where() method 

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array in_arr1 
in_arr1 = geek.arange(4)
print ("1st Input array : ", in_arr1)

# applying MaskedArray.masked_where methods 
# to input array in_arr1 where value = 1
mask_arr1 = ma.masked_where(in_arr1 == 1, in_arr1)
print ("1st Masked array : ", mask_arr1)

# creating input array in_arr2 
in_arr2 = geek.arange(4)
print ("2nd Input array : ", in_arr2)

# applying MaskedArray.masked_where methods 
# to input array in_arr2 where value = 1
mask_arr2 = ma.masked_where(in_arr2 == 3, in_arr2)
print ("2nd Masked array : ", mask_arr2)

# applying MaskedArray.masked_where methods 
# to 1st masked array where second masked array
# is used as condition
res_arr = ma.masked_where(mask_arr1 == 3, mask_arr2)
print("Resultant Masked array : ", res_arr)
```

**Output:**

```
1st Input array :  [0 1 2 3]
1st Masked array :  [0 -- 2 3]
2nd Input array :  [0 1 2 3]
2nd Masked array :  [0 1 2 --]
Resultant Masked array :  [0 -- 2 --]

```
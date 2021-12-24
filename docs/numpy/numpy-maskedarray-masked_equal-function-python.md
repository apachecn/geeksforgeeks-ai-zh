# Numpy maskedarray . masked _ equal()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-masked _ equal-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-masked_equal-function-python/)

在许多情况下，数据集可能是不完整的，或者被无效数据污染。例如，传感器可能未能记录数据，或者记录了无效值。`numpy.ma`模块通过引入屏蔽数组提供了一种解决这个问题的便捷方法。屏蔽数组是指可能缺少条目或条目无效的数组。

**`numpy.MaskedArray.masked_equal()`** 函数用于屏蔽一个数组中等于给定值的地方。

> **语法:** `numpy.ma.masked_equal(arr, value, copy=True)`
> 
> **参数:**
> **arr:**【ndarray】输入我们要屏蔽的数组。
> **值:**【int】我们要屏蔽的屏蔽数组的元素。
> **复制:**【bool】如果为真(默认)，在结果中复制一份 arr。如果为假，就地修改 arr 并返回视图。
> 
> **返回:**【屏蔽阵列】屏蔽的结果。

**代码#1 :**

```py
# Python program explaining
# numpy.MaskedArray.masked_equal() method 

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array 
in_arr = geek.array([1, 2, 3, -1, 2])
print ("Input array : ", in_arr)

# applying MaskedArray.masked_equal methods 
# to input array where value = 2
mask_arr = ma.masked_equal(in_arr, 2)
print ("Masked array : ", mask_arr)
```

**Output:**

```py
Input array :  [ 1  2  3 -1  2]
Masked array :  [1 -- 3 -1 --]

```

**代码#2 :**

```py
# Python program explaining
# numpy.MaskedArray.masked_equal() method 

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array 
in_arr = geek.array([2e8, 3e-5, -45.0, 2e5, 5e2])
print ("Input array : ", in_arr)

# applying MaskedArray.masked_equal methods 
# to input array where value = 5e2
mask_arr = ma.masked_equal(in_arr, 5e2)
print ("Masked array : ", mask_arr)
```

**Output:**

```py
Input array :  [ 2.0e+08  3.0e-05 -4.5e+01  2.0e+05  5.0e+02]
Masked array :  [200000000.0 3e-05 -45.0 200000.0 --]

```
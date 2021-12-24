# Numpy MaskedArray masked _ out()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-masked _ external-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-masked_outside-function-python/)

**`numpy.MaskedArray.masked_outside()`** 功能用于屏蔽给定区间外的数组。该功能是屏蔽的快捷方式，在间隔`[v1, v2] (arr <v1)|(arr > v2)`之外的 arr 条件为真。边界 v1 和 v2 可以按任意顺序给出。

> **语法:** `numpy.ma.masked_outside(arr, v1, v2, copy=True)`
> 
> **参数:**
> **arr:**【ndarray】输入我们要屏蔽的数组。
> **v1、v2:**【int】上下范围。
> **复制:**【bool】如果为真(默认)，在结果中复制一份 arr。如果为假，就地修改 arr 并返回视图。
> 
> **返回:**【屏蔽数组】屏蔽后的结果数组。

**代码#1 :**

```
# Python program explaining
# numpy.MaskedArray.masked_outside() method 

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array 
in_arr = geek.array([1, 2, 3, -1, 2])
print ("Input array : ", in_arr)

# applying MaskedArray.masked_outside methods 
mask_arr = ma.masked_outside(in_arr, -1, 1)
print ("Masked array : ", mask_arr)
```

**Output:**

```
Input array :  [ 1  2  3 -1  2]
Masked array :  [1 -- -- -1 --]

```

**代码#2 :**

```
# Python program explaining
# numpy.MaskedArray.masked_outside() method 

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

# creating input array 
in_arr = geek.array([5e8, 3e-5, -45.0, 4e4, 5e2])
print ("Input array : ", in_arr)

# applying MaskedArray.masked_outside methods 
mask_arr = ma.masked_outside(in_arr, 5e2, 5e8)
print ("Masked array : ", mask_arr)
```

**Output:**

```
Input array :  [ 5.0e+08  3.0e-05 -4.5e+01  4.0e+04  5.0e+02]
Masked array :  [500000000.0 -- -- 40000.0 500.0]

```
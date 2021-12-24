# numpy.ma.mask_rows()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-ma-mask _ rows-function-python/](https://www.geeksforgeeks.org/numpy-ma-mask_rows-function-python/)

在这个**函数中，屏蔽包含屏蔽值的 2D 数组的行。这个函数是 mask_rowcols 轴等于 0 的快捷方式。** 

> **语法:** numpy.ma.mask_rows(arr，axis = None)
> **参数:**
> **arr:**【array _ like，MaskedArray】要屏蔽的数组。结果是一个掩码数组。
> **轴:**【int，可选】执行操作的轴。默认值为无。
> **返回:**【掩码数组】输入数组的修改版本。

**代码#1 :**

## 蟒蛇 3

```
# Python program explaining
# numpy.ma.mask_rows() function

# importing numpy as geek
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

arr = geek.zeros((4, 4), dtype = int)
arr[2, 2] = 1

arr = ma.masked_equal(arr, 1)

gfg = ma.mask_rows(arr)

print (gfg)
```

**输出:**

```
[[0 0 0 0]
 [0 0 0 0]
 [-- -- -- --]
 [0 0 0 0]]
```

**代码#2 :**

## 蟒蛇 3

```
# Python program explaining
# numpy.ma.mask_rows() function

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

arr = geek.zeros((5, 5), dtype = int)
arr[3, 3] = 1

arr = ma.masked_equal(arr, 1)

gfg = ma.mask_rows(arr)

print (gfg)
```

**输出:**

```
[[0 0 0 0 0]
 [0 0 0 0 0]
 [0 0 0 0 0]
 [-- -- -- -- --]
 [0 0 0 0 0]]
```
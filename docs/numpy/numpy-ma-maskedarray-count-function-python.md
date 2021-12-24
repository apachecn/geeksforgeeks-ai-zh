# numpy . ma . maskearray . count()函数–Python

> 原文:[https://www . geeksforgeeks . org/numpy-ma-masked array-count-function-python/](https://www.geeksforgeeks.org/numpy-ma-maskedarray-count-function-python/)

**`numpy.ma.MaskedArray.count()`** 函数沿着给定的轴计算数组中未被屏蔽的元素。

> **语法:**numpy . ma . maskearray . count(self，axis=None，keepdims = no value)
> 
> **参数:**
> **轴:**【无或整数或整数元组，可选】执行计数的轴。默认轴为无，在输入数组的所有维度上执行计数。轴可以是负的，在这种情况下，它从最后一个轴计数到第一个轴。
> **保持尺寸:**【bool，可选】如果设置为真，缩小的轴将作为尺寸为 1 的尺寸留在结果中。使用此选项，结果将针对阵列正确广播。
> 
> **返回:**【n 数组或标量】一个与输入数组形状相同的数组，去掉指定的轴。如果数组是 0-d 数组，或者如果轴是无，则返回标量。

**代码#1 :**

```py
# Python program explaining
# numpy.ma.MaskedArray.count() function

# importing numpy as geek   
# and numpy.ma module as ma  
import numpy as geek  
import numpy.ma as ma

arr = ma.arange(6).reshape((2, 3))
arr[1, :] = ma.masked

gfg = arr.count(axis = 0)

print (gfg)
```

**输出:**

```py
[1 1 1]

```

**代码#2 :**

```py
# Python program explaining
# numpy.ma.MaskedArray.count() function

# importing numpy as geek   
# and numpy.ma module as ma  
import numpy as geek  
import numpy.ma as ma

arr = ma.arange(6).reshape((2, 3))
arr[1, :] = ma.masked

gfg = arr.count()

print (gfg)
```

**输出:**

```py
3

```
# Numpy maskearray . filled()方法–Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-filled-method-python/](https://www.geeksforgeeks.org/numpy-maskedarray-filled-method-python/)

**`numpy.MaskedArray.filled()`** 函数返回一个 self 的副本，用给定的值填充被屏蔽的值。但是，如果没有要填充的掩码值，self 将作为数组返回。

> **语法:** numpy。MaskedArray.filled(自身，fill_value =无)
> 
> **参数:**
> **fill_value :** 【标量，可选】用于无效条目的值，默认为无。如果为“无”，则改为使用数组的 fill_value 属性。
> 
> **返回:**
> **filled _ array:**【n array】将无效条目替换为 fill_value 的 self 副本，如果没有要替换的无效条目，则将 self 本身作为 n array。

**代码#1 :**

```py
# Python program explaining
# numpy.MaskedArray.filled() function

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma

arr = geek.ma.array([2, 4, 6, 8, 10], mask =[0, 0, 1, 0, 1],
                                          fill_value = -999)
gfg = arr.filled()

print(gfg)
```

**输出:**

```py
[   2    4 -999    8 -999]

```

**代码#2 :**

```py
# Python program explaining
# numpy.MaskedArray.filled() function

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma

arr = geek.ma.array([1, 2, 3, 4, 5], mask =[1, 0, 1, 0, 0], 
                                         fill_value = -999)
gfg = arr.filled()

print(gfg)
```

**输出:**

```py
[-999    2 -999    4    5]

```
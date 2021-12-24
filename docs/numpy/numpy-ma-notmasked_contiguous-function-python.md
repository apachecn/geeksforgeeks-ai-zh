# numpy . ma . notmasked _ contact 函数| Python

> 原文:[https://www . geesforgeks . org/numpy-ma-notmasked _ continental-function-python/](https://www.geeksforgeeks.org/numpy-ma-notmasked_contiguous-function-python/)

**`numpy.ma.notmasked_contiguous()`** 函数沿着给定的轴查找掩码数组中连续的未掩码数据。

> **语法:**numpy . ma . notmasked _ contact(arr，axis = None)
> 
> **参数:**
> **arr :** 【阵 _ 象】输入阵。
> **轴:**【int，可选】执行操作的轴。默认值为无。
> 
> **返回:**【列表】数组中未屏蔽索引的切片(开始和结束索引)列表。如果输入是 2d，并且指定了轴，则结果是列表列表。

**代码#1 :**

```
# Python program explaining
# numpy.ma.notmasked_contiguous() function

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

arr = geek.arange(12).reshape((3, 4))
mask = geek.zeros_like(arr)
mask[1:, :-1] = 1; mask[0, 1] = 1; mask[-1, 0] = 0
ma = geek.ma.array(arr, mask = mask)

gfg = geek.ma.notmasked_contiguous(ma)

print (gfg)
```

**输出:**

> [切片(0，1，无)，切片(2，4，无)，切片(7，9，无)，切片(11，12，无)]

**代码#2 :**

```
# Python program explaining
# numpy.ma.notmasked_contiguous() function

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

arr = geek.arange(12).reshape((3, 4))
mask = geek.zeros_like(arr)
mask[1:, :-1] = 1; mask[0, 1] = 1; mask[-1, 0] = 0
ma = geek.ma.array(arr, mask = mask)

gfg = geek.ma.notmasked_contiguous(ma, axis = 1)

print (gfg)
```

**输出:**

> [[切片(0，1，无)，切片(2，4，无)]，[切片(3，4，无)]，[切片(0，1，无)，切片(3，4，无)]
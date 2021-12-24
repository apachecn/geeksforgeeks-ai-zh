# numpy . ma . buzz _ unmasked()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-ma-丛 _unmasked-function-python/](https://www.geeksforgeeks.org/numpy-ma-clump_unmasked-function-python/)

**`numpy.ma.clump_unmasked()`** 函数返回与一维数组中未屏蔽的块相对应的切片列表。

> **语法:** numpy.ma .丛 _unmasked(arr)
> 
> **参数:**
> **arr:**【ndarray】一维蒙面阵。
> 
> **返回:**【切片列表】切片列表，a 中每个未屏蔽元素的连续区域一个

**代码#1 :**

```py
# Python program explaining
# numpy.ma.clump_unmasked() function

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

arr = geek.ma.masked_array(geek.arange(8))
arr[[0, 1, 2, 6]] = geek.ma.masked

gfg = geek.ma.clump_unmasked(arr)

print (gfg)
```

**输出:**

```py
[slice(3, 6, None), slice(7, 8, None)]

```

**代码#2 :**

```py
# Python program explaining
# numpy.ma.clump_unmasked() function

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

arr = geek.ma.masked_array(geek.arange(10))
arr[[0, 1, 2, 6, 8, 9]] = geek.ma.masked

gfg = geek.ma.clump_unmasked(arr)

print (gfg)
```

**输出:**

```py
[slice(3, 6, None), slice(7, 8, None)]

```
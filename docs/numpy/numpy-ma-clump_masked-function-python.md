# numpy . ma . buzz _ masked()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-ma-丛 _masked-function-python/](https://www.geeksforgeeks.org/numpy-ma-clump_masked-function-python/)

**`numpy.ma.clump_masked()`** 函数返回一个切片列表，该列表对应于一维数组中被屏蔽的块。

> **语法:** numpy.ma .丛 _masked(arr)
> 
> **参数:**
> **arr:**【ndarray】一维蒙面阵。
> 
> **返回:**【切片列表】切片列表，arr 中屏蔽元素的每个连续区域一个。

**代码#1 :**

```
# Python program explaining
# numpy.ma.clump_masked() function

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

arr = geek.ma.masked_array(geek.arange(8))
arr[[0, 1, 2, 6]] = geek.ma.masked

gfg = geek.ma.clump_masked(arr)

print (gfg)
```

**输出:**

```
[slice(0, 3, None), slice(6, 7, None)]

```

**代码#2 :**

```
# Python program explaining
# numpy.ma.clump_masked() function

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

arr = geek.ma.masked_array(geek.arange(10))
arr[[0, 1, 2, 6, 8, 9]] = geek.ma.masked

gfg = geek.ma.clump_masked(arr)

print (gfg)
```

**输出:**

```
[slice(0, 3, None), slice(6, 7, None), slice(8, 10, None)]

```
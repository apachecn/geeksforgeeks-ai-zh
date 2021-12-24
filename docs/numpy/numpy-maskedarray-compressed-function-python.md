# Numpy maskearray . compressed()函数–Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-compressed-function-python/](https://www.geeksforgeeks.org/numpy-maskedarray-compressed-function-python/)

**`numpy.MaskedArray.compressed()`** 函数将所有未屏蔽的数据作为一维数组返回。

> **语法:** numpy。MaskedArray.compressed(自)
> 
> **返回:**【n 数组】返回一个保存未屏蔽数据的新数组。

**代码#1 :**

```
# Python program explaining
# numpy.MaskedArray.compressed() function

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma

arr = geek.ma.array(geek.arange(10), mask =[0]*6 + [1]*4)
gfg = arr.compressed()

print(gfg)
```

**输出:**

```
[0 1 2 3 4 5]

```

**代码#2 :**

```
# Python program explaining
# numpy.MaskedArray.compressed() function

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma

arr = geek.ma.array(geek.arange(7), mask =[0]*4 + [1]*3)
gfg = arr.compressed()

print(gfg)
```

**输出:**

```
[0 1 2 3]

```
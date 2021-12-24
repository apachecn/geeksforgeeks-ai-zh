# numpy . ma . maskearray . tolist()函数–Python

> 原文:[https://www . geeksforgeeks . org/numpy-ma-masked array-to list-function-python/](https://www.geeksforgeeks.org/numpy-ma-maskedarray-tolist-function-python/)

**`numpy.ma.MaskedArray.tolist()`** 函数将屏蔽数组的数据部分作为分层 Python 列表返回。

> **语法:**numpy . ma . maskedarray . to list(fill _ value = None)
> 
> **参数:**
> **轴:**【标量，可选】用于无效条目的值。默认值为无。
> 
> **返回:**【列表】屏蔽数组的 Python 列表表示。

**代码#1 :**

```py
# Python program explaining
# numpy.ma.MaskedArray.tolist() function

# importing numpy as geek   
# and numpy.ma module as ma  
import numpy as geek  
import numpy.ma as ma

arr = geek.ma.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]],
                               mask =[0] + [1, 0] * 4)

gfg = arr.tolist()

print (gfg)
```

**输出:**

```py
[[1, None, 3], [None, 5, None], [7, None, 9]]

```

**代码#2 :**

```py
# Python program explaining
# numpy.ma.MaskedArray.tolist() function

# importing numpy as geek   
# and numpy.ma module as ma  
import numpy as geek  
import numpy.ma as ma

arr = geek.ma.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]],
                              mask =[0] + [1, 0] * 4)

gfg = arr.tolist(-999)

print (gfg)
```

**输出:**

```py
[[1, -999, 3], [-999, 5, -999], [7, -999, 9]]

```
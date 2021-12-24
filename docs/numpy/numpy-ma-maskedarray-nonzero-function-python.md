# numpy . ma . maskearray .非零()函数–Python

> 原文:[https://www . geeksforgeeks . org/numpy-ma-masked array-非零-function-python/](https://www.geeksforgeeks.org/numpy-ma-maskedarray-nonzero-function-python/)

**`numpy.ma.MaskedArray.nonzero()`** 函数返回不为零的未屏蔽元素的索引。这个函数返回一组数组，每个维度一个数组，包含该维度中非零元素的索引。

> **语法:** numpy.ma.MaskedArray .非零(自)
> 
> **返回:**【元组】非零元素的索引。

**代码#1 :**

```py
# Python program explaining
# numpy.ma.MaskedArray.nonzero() function

# importing numpy as geek   
# and numpy.ma module as ma  
import numpy as geek  
import numpy.ma as ma

arr = ma.array(geek.eye(5))

gfg = arr.nonzero()

print (gfg)
```

**输出:**

```py
(array([0, 1, 2, 3, 4]), array([0, 1, 2, 3, 4]))

```

**代码#2 :**

```py
# Python program explaining
# numpy.ma.MaskedArray.nonzero() function

# importing numpy as geek   
# and numpy.ma module as ma  
import numpy as geek  
import numpy.ma as ma

arr = ma.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

gfg = ma.nonzero(arr > 3)

print (gfg)
```

**输出:**

```py
(array([1, 1, 1, 2, 2, 2]), array([0, 1, 2, 0, 1, 2]))

```
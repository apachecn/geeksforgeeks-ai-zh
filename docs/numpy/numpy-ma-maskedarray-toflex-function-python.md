# numpy . ma . maskearray . toflex()函数–Python

> 原文:[https://www . geeksforgeeks . org/numpy-ma-masked array-toflex-function-python/](https://www.geeksforgeeks.org/numpy-ma-maskedarray-toflex-function-python/)

**`numpy.ma.MaskedArray.toflex()`** 函数将一个屏蔽数组转换成一个灵活类型的数组。返回的灵活类型数组将有两个字段:数据字段和掩码字段。数据字段存储数组的数据部分，掩码字段存储数组的掩码部分。

> **语法:**numpy . ma . maskearray . toflex(self)
> 
> **Return:**【ndarray】一个新的灵活类型的 ndarray，有两个字段:第一个元素包含一个值，第二个元素包含对应的 mask boolean。返回的记录形状与 self.shape 匹配。

**代码#1 :**

```
# Python program explaining
# numpy.ma.MaskedArray.toflex() function

# importing numpy as geek 
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

arr = geek.ma.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]], 
                                 mask =[0] + [1, 0]*4)

gfg = arr.toflex()

print (gfg)
```

**输出:**

```
[[(1, False) (2,  True) (3, False)]
 [(4,  True) (5, False) (6,  True)]
 [(7, False) (8,  True) (9, False)]]

```

**代码#2 :**

```
# Python program explaining
# numpy.ma.MaskedArray.toflex() function

# importing numpy as geek 
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

arr = geek.ma.array([[11, 12, 13], [14, 15, 16], [17, 18, 19]], 
                                         mask =[0] + [1, 1]*4)

gfg = arr.toflex()

print (gfg)
```

**输出:**

```
[[(11, False) (12,  True) (13,  True)]
 [(14,  True) (15,  True) (16,  True)]
 [(17,  True) (18,  True) (19,  True)]]

```
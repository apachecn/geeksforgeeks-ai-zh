# numpy.ma.masked_all()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-ma-masked _ all-function-python/](https://www.geeksforgeeks.org/numpy-ma-masked_all-function-python/)

**`numpy.ma.masked_all()`** 函数返回一个给定形状和数据类型的空掩码数组，其中所有数据都被掩码。

> **语法:** numpy.ma.masked_all(shape，dtype)
> 
> **参数:**
> **形状:**【元组】所需 MaskedArray 的形状。
> **数据类型:**【数据类型，可选】输出的数据类型。
> 
> **返回:**【屏蔽数组】一个屏蔽了所有数据的屏蔽数组。

**代码#1 :**

```
# Python program explaining
# numpy.ma.masked_all() function

# importing numpy as geek 
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

gfg = ma.masked_all((4, 4))

print (gfg)
```

**输出:**

```
[[-- -- -- --]
 [-- -- -- --]
 [-- -- -- --]
 [-- -- -- --]]

```

**代码#2 :**

```
# Python program explaining
# numpy.ma.masked_all() function

# importing numpy as geek 
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

gfg = ma.masked_all((3, 3), dtype = geek.int32)

print (gfg)
```

**输出:**

```
[[-- -- --]
 [-- -- --]
 [-- -- --]]

```
# numpy.ma.masked_all_like()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-ma-masked _ all _ like-function-python/](https://www.geeksforgeeks.org/numpy-ma-masked_all_like-function-python/)

**`numpy.ma.masked_all_like()`** 函数返回一个与 arr 数组相同形状和数据类型的空掩码数组，其中所有数据都被掩码。

> **语法:**numpy . ma . masked _ all _ like(arr)
> 
> **参数:**
> **arr:**【ndarray】描述所需掩码数组的形状和数据类型的数组。
> 
> **返回:**【屏蔽数组】一个屏蔽了所有数据的屏蔽数组。

**代码#1 :**

```
# Python program explaining
# numpy.ma.masked_all_like() function

# importing numpy as geek 
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

arr = geek.zeros((4, 4), dtype = geek.float32)

gfg = ma.masked_all_like(arr)

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
# numpy.ma.masked_all_like() function

# importing numpy as geek 
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

arr = geek.zeros((4, 3), dtype = geek.float32)

gfg = ma.masked_all_like(arr)

print (gfg)
```

**输出:**

```
[[-- -- --]
 [-- -- --]
 [-- -- --]
 [-- -- --]]

```
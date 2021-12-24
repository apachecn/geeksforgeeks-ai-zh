# numpy.ma.make_mask_none()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-ma-make _ mask _ none-function-python/](https://www.geeksforgeeks.org/numpy-ma-make_mask_none-function-python/)

**`numpy.ma.make_mask_none()`** 函数返回一个给定形状的布尔掩码，用 False 填充。
此函数返回一个布尔数组，所有条目都为假，可用于常见的掩码操作。如果指定了复杂的数据类型，则每个字段的类型都将转换为布尔类型。

> **语法:**numpy . ma . make _ mask _ None(new shape，dtype = None)
> 
> **参数:**
> **新形状:**【元组】表示面具形状的元组。
> **数据类型:**[{无，数据类型}，可选]默认情况下，数据类型为无。否则，使用一个新的数据类型，其字段与转换为布尔类型的数据类型相同。
> 
> **返回:**【n 数组】适当形状和数据类型的数组，用 False 填充。

**代码#1 :**

```py
# Python program explaining
# numpy.ma.make_mask_none() function

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

gfg = ma.make_mask_none(4)

print (gfg)
```

**输出:**

```py
[False False False False]

```

**代码#2 :**

```py
# Python program explaining
# numpy.ma.make_mask_none() function

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

gfg = ma.make_mask_none(4, dtype = None)

print (gfg)
```

**输出:**

```py
[False False False False]

```
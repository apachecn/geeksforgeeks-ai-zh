# numpy.ma.is_mask()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-ma-is _ mask-function-python/](https://www.geeksforgeeks.org/numpy-ma-is_mask-function-python/)

**`numpy.ma.is_mask()`** 函数如果参数 m 是有效的标准掩码，则返回 True。这个函数不检查输入的内容，只检查类型是否为 MaskType。特别是，如果掩码具有灵活的数据类型，此函数将返回 False。

> **语法:** numpy.ma.is_mask(m)
> 
> **参数:**
> **m :** 【阵 _ 象】阵对查。
> **返回:**【bool】如果 m.dtype.type 为 MaskType，则返回 True，否则返回 False。

**代码#1 :**

```py
# Python program explaining
# numpy.ma.is_mask() function

# importing numpy as geek 
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

m = ma.masked_equal([0, 1, 2, 0, 3], 0)

gfg = ma.is_mask(m)

print (gfg)
```

**输出:**

```py
False

```

**代码#2 :**

```py
# Python program explaining
# numpy.ma.is_mask() function

# importing numpy as geek 
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

m = [True, False, True]

gfg = ma.is_mask(m)

print (gfg)
```

**输出:**

```py
False

```
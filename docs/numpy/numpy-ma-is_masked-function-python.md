# numpy.ma.is_masked()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-ma-is _ masked-function-python/](https://www.geeksforgeeks.org/numpy-ma-is_masked-function-python/)

**`numpy.ma.is_masked()`** 函数确定输入是否有屏蔽值&接受任何对象作为输入，但总是返回 False，除非输入是包含屏蔽值的屏蔽数组。

> **语法:** numpy.ma.is_masked(arr)
> 
> **参数:**
> **arr:**【Array _ like】数组检查屏蔽值。
> 
> **返回:**【bool】如果 arr 是带掩码值的掩码数组，则返回 True，否则返回 False。

**代码#1 :**

```py
# Python program explaining
# numpy.ma.is_masked() function

# importing numpy as geek 
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

arr = ma.masked_equal([0, 1, 2, 0, 3], 0)

gfg = ma.is_masked(arr)

print (gfg)
```

**输出:**

```py
True

```

**代码#2 :**

```py
# Python program explaining
# numpy.ma.is_masked() function

# importing numpy as geek 
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

arr = [True, False, True]

# always returns False unless
# the input is a MaskedArray 
gfg = ma.is_masked(arr)

print (gfg)
```

**输出:**

```py
False

```
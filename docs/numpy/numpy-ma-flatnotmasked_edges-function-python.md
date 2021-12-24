# numpy . ma . flat notmasked _ edges()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-ma-flat notmasked _ edges-function-python/](https://www.geeksforgeeks.org/numpy-ma-flatnotmasked_edges-function-python/)

**`numpy.ma.flatnotmasked_edges()`** 函数查找第一个和最后一个未屏蔽值的索引。

> **语法:**num py . ma . flatnotmasked _ edges(arr)
> 
> **参数:**
> **arr:**【array _ like】输入一维 MaskedArray。
> 
> **返回:**【非数组或无】数组中第一个和最后一个非掩码值的索引。如果所有值都被屏蔽，则返回无。

**代码#1 :**

```
# Python program explaining
# numpy.ma.flatnotmasked_edges() function

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

arr = geek.ma.arange(12)

gfg = geek.ma.flatnotmasked_edges(arr)

print (gfg)
```

**输出:**

```
[ 0, 11]

```

**代码#2 :**

```
# Python program explaining
# numpy.ma.flatnotmasked_edges() function

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

arr = geek.ma.arange(12)
arr[:] = geek.ma.masked

gfg = geek.ma.flatnotmasked_edges(arr)

print (gfg)
```

**输出:**

```
None

```
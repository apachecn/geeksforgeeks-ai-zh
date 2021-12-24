# numpy.ma.notmasked_edges()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-ma-notmasked _ edges-function-python/](https://www.geeksforgeeks.org/numpy-ma-notmasked_edges-function-python/)

**`numpy.ma.notmasked_edges()`** 函数沿轴查找第一个和最后一个未屏蔽值的索引。
如果所有值都被屏蔽，则返回无。否则，返回一个二元组列表，分别对应于第一个和最后一个未屏蔽值的索引。

> **语法:**numpy . ma . notmasked _ edges(arr，axis = None)
> 
> **参数:**
> **arr :** 【阵 _ 象】输入阵。
> **轴:**【int，可选】执行操作的轴。默认值为无。
> 
> **返回:**【n 数组或列表】如果数组中有任何屏蔽数据，则返回开始和结束索引的数组。如果数组中没有屏蔽数据，edges 是第一个和最后一个索引的列表。

**代码#1 :**

```py
# Python program explaining
# numpy.ma.notmasked_edges() function

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

arr = geek.arange(12).reshape((3, 4))

gfg = geek.ma.notmasked_edges(arr)

print (gfg)
```

**输出:**

```py
[ 0, 11]

```

**代码#2 :**

```py
# Python program explaining
# numpy.ma.notmasked_edges() function

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

arr = geek.arange(12).reshape((3, 4))
m = geek.zeros_like(arr)
m[1:, 1:] = 1

am = geek.ma.array(arr, mask = m)

gfg = geek.ma.notmasked_edges(am)

print (gfg)
```

**输出:**

```py
[0, 8]

```
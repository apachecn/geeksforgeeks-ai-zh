# numpy . ma . flat notmasked _ contact()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-ma-flat notmasked _ contact-function-python/](https://www.geeksforgeeks.org/numpy-ma-flatnotmasked_contiguous-function-python/)

**numpy . ma . flat notmasked _ continuous()**函数沿给定轴查找掩码数组中连续的未掩码数据。

> **语法:**numpy . ma . flat notmasked _ contact(arr)
> **参数:**
> **arr:**【array _ like】输入数组。
> **返回:**【切片 _ 列表】切片对象的排序序列(开始索引、结束索引)。

**代码#1 :**

## 蟒蛇 3

```py
# Python program explaining
# numpy.ma.flatnotmasked_contiguous() function

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

arr = geek.ma.arange(8)

gfg = geek.ma.flatnotmasked_contiguous(arr)

print (gfg)
```

**输出:**

```py
slice(0, 8, None)
```

**代码#2 :**

## 蟒蛇 3

```py
# Python program explaining
# numpy.ma.flatnotmasked_contiguous() function

# importing numpy as geek 
# and numpy.ma module as ma
import numpy as geek
import numpy.ma as ma

arr = geek.ma.arange(12)

gfg = geek.ma.flatnotmasked_contiguous(arr)

print (gfg)
```

**输出:**

```py
slice(0, 12, None)
```
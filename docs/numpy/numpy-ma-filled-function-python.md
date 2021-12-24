# numpy.ma.filled()函数–Python

> 原文:[https://www . geesforgeks . org/numpy-ma-filled-function-python/](https://www.geeksforgeeks.org/numpy-ma-filled-function-python/)

**`numpy.ma.filled()`** 函数以数组形式返回输入，用填充值替换屏蔽数据。如果 arr 不是 MaskedArray，则返回 arr 本身。如果 arr 是掩码数组，fill_value 是无，fill_value 设置为 arr.fill_value。

> **语法:** numpy.ma.filled(arr，fill_value = None)
> 
> **参数:**
> **arr:**【maskearray 或 array_like】一个输入对象。
> **fill_value :** 【标量，可选】Filling 值。默认值为无。
> 
> **返回:**【ndarray】填充的数组。

**代码#1 :**

```py
# Python program explaining
# numpy.ma.filled() function

# importing numpy as geek   
# and numpy.ma module as ma  
import numpy as geek  
import numpy.ma as ma

arr = geek.ma.array(geek.arange(4).reshape(2, 2),
                         mask =[[1, 0], [0, 1]])

gfg = arr.filled()

print (gfg)
```

**输出:**

```py
[[999999      1]
 [     2 999999]]

```

**代码#2 :**

```py
# Python program explaining
# numpy.ma.filled() function

# importing numpy as geek   
# and numpy.ma module as ma  
import numpy as geek  
import numpy.ma as ma

arr = geek.ma.array(geek.arange(9).reshape(3, 3), 
          mask =[[1, 0, 0], [1, 0, 0], [0, 0, 0]])

gfg = arr.filled()

print (gfg)
```

**输出:**

```py
[[999999      1      2]
 [999999      4      5]
 [     6      7      8]]

```
# numpy.ma.masked_values()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-ma-masked _ values-function-python/](https://www.geeksforgeeks.org/numpy-ma-masked_values-function-python/)

**`numpy.ma.masked_values()`** 函数返回一个 MaskedArray，其中被屏蔽的数组 arr 中的数据大约等于使用 isclose 确定的值。masked_values 的默认容差与 isclose 的容差相同。

> **语法:** numpy.ma.masked_values(arr，value，rtol = 1e-05，atol = 1e-08，copy = True，shrink = True)
> 
> **参数:**
> **arr :** 【阵 _ 象】阵对掩。
> **值:**【浮动】掩蔽值。
> **rtol，环礁:**【float，可选】必须可转换为与数据形状相同的布尔数组。True 表示屏蔽的数据。
> **副本:**【bool，可选】是否返回 arr 副本。
> **收缩:**【bool，可选】是否将满是 False 的蒙版折叠为 nomask。
> 
> **返回:**【屏蔽数组】屏蔽数组的结果，其中近似等于值。

**代码#1 :**

```py
# Python program explaining
# numpy.ma.masked_values() function

# importing numpy as geek 
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma

arr = geek.array([1, 1.5, 2, 1.5, 3])

gfg = ma.masked_values(arr, 1.5)

print (gfg)
```

**输出:**

```py
[1.0 -- 2.0 -- 3.0]

```

**代码#2 :**

```py
# Python program explaining
# numpy.ma.masked_values() function

# importing numpy as geek 
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma

arr = geek.array([1, 2, 3, 4, 5, 6])

gfg = ma.masked_values(arr, 4)

print (gfg)
```

**输出:**

```py
[1 2 3 -- 5 6]

```
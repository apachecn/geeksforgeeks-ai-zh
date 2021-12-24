# numpy.interp()函数–Python

> 原文:[https://www.geeksforgeeks.org/numpy-interp-function-python/](https://www.geeksforgeeks.org/numpy-interp-function-python/)

**`numpy.interp()`** 函数将一维分段线性插值返回给定离散数据点(xp，fp)的函数，在 x 处求值。

> **语法:** numpy.interp(x，xp，fp，左=无，右=无，句点=无)
> 
> **参数:**
> **x :** 【类数组】评估插值的 x 坐标。
> **xp:** 【一维浮动序列】如果没有指定参数周期，数据点的 x 坐标必须增加。否则，在用 xp = xp % period 规范化周期边界后，xp 在内部排序。
> **fp :** 【浮点或复数的一维序列】数据点的 y 坐标，长度与 xp 相同。
> **左:**【FP 对应的可选浮点或复数】x < xp[0]返回的值，默认为 fp[0]。
> **右:**【FP 对应的可选浮点数或复数】x 要返回的值> xp[-1]，默认为 fp[-1]。
> **周期:**【无或浮动，可选】x 坐标的周期。该参数允许角度 x 坐标的适当插值。如果指定了周期，则忽略左右参数。
> 
> **返回:**【浮点或复数或数组】插值，形状与 x 相同

**代码#1 :**

```py
# Python program explaining
# numpy.interp() function

# importing numpy as geek 
import numpy as geek 

x = 3.6
xp = [2, 4, 6]
fp = [1, 3, 5]

gfg = geek.interp(x, xp, fp)

print (gfg)
```

**输出:**

```py
2.6

```

**代码#2 :**

```py
# Python program explaining
# numpy.interp() function

# importing numpy as geek 
import numpy as geek 

x = [0, 1, 2.5, 2.72, 3.14]
xp = [2, 4, 6]
fp = [1, 3, 5]

gfg = geek.interp(x, xp, fp)

print (gfg)
```

**输出:**

```py
[1\.   1\.   1.5  1.72 2.14]

```
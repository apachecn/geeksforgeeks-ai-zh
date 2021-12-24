# sciPy stats.threshold()函数| Python

> 原文:[https://www . geesforgeks . org/scipy-stats-threshold-function-python/](https://www.geeksforgeeks.org/scipy-stats-threshold-function-python/)

**scipy.stats.threshold(a，threshmin =无，threshmax =无，newval=0)** 函数裁剪给定数组。超出设定限值的值可以用“newval”参数代替。

> **参数:**
> **arr:**【array _ like】输入要剪辑的数组或对象。
> **阈值:**(浮点，整数)最小阈值。默认为无
> **阈值最大值:**(浮点，整数)最大阈值。默认情况下为无
> **新值:**(浮点，整数)值代替值(超出限制)。
> 
> **结果:**用 newval 替换值(超出限制)的裁剪数组。

**代码#1:工作**

```py
# stats.threshold() method  
import numpy as np
from scipy import stats

arr1 = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

print ("\narr1 : ", arr1)

print ("\nclipped arr1 : \n", stats.threshold(
        arr1, threshmin = 2, threshmax = 8, newval =-1))
```

**输出:**

```py
arr1 :  [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

clipped arr1 : 
[-1 -1 2 3 4 5 6 7 8 -1]

```
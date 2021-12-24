# sciPy stats.itemfreq()函数| Python

> 原文:[https://www . geesforgeks . org/scipy-stats-item freq-function-python/](https://www.geeksforgeeks.org/scipy-stats-itemfreq-function-python/)

**scipy.stats.itemfreq(arr，axis = None)** 功能帮助我们计算物品频率。

> **参数:**
> **arr:**【array _ like】输入数组。
> **结果:** 2D 阵同项频率。

**代码#1:** 变异的使用()

## 蟒蛇 3

```
# cummulative frequency
from scipy import stats
import numpy as np 

arr = [14, 31, 27, 27, 31, 13, 14, 13] 

print ("Itemfrequency : \n", stats.itemfreq(arr))

print ("\n\nBincount : \n", np.bincount(arr))
```

**Output:** 

```
Itemfrequency : 
 [[13  2]
 [14  2]
 [27  2]
 [31  2]]

Bincount : 
 [0 0 0 0 0 0 0 0 0 0 0 0 0 2 2 0 0 0 0 0 0 0 0 0 0 0 0 2 0 0 0 2]
```
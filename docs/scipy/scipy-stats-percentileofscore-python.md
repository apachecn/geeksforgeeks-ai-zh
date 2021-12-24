# scipy stats . percentile ofscore()| python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/scipy-stats-percentile of ofscore-python/

**scipy . stats . percentileofscore(a，score，kind='rank')** 函数帮助我们计算分数相对于分数列表的百分位数排名。
假设 x 的百分位数是 60%，这意味着 a 中 80%的分数低于 x。

> **参数:**
> **arr:**【array _ like】输入数组。
> **得分:**【int 或 float】与数组中元素相比的得分。
> **种类:**【可选】【等级】【弱】【严】【中】【中】。
> **结果:**相对于数组元素的分数百分位数。

**代码#1:**

## 蟒蛇 3

```py
# percentileofscore
from scipy import stats
import numpy as np

# 1D array 
arr = [20, 2, 7, 1, 7, 7, 34]
print("arr : ", arr) 

print ("\nPercentile of 7  : ", stats.percentileofscore(arr, 7))

print ("\nPercentile of 34 : ", stats.percentileofscore(arr, 34))

print ("\nPercentile of 2  : ", stats.percentileofscore(arr, 2))
```

**输出:**

```py
arr :  [20, 2, 7, 1, 7, 7, 34]

Percetile of 7  :  57.1428571429

Percetile of 34 :  100.0

Percetile of 2  :  28.5714285714
```
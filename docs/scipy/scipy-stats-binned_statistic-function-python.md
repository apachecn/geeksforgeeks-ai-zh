# sciPy stats . binned _ statistics()函数| Python

> 原文:[https://www . geesforgeks . org/scipy-stats-binned _ statistics-function-python/](https://www.geeksforgeeks.org/scipy-stats-binned_statistic-function-python/)

`**stats.binned_statistic(x, values, statistic='mean', bins=10, range=None)**`函数计算给定数据(数组元素)的入库统计值。
工作原理类似于[直方图](https://www.geeksforgeeks.org/scipy-stats-histogram-function-python/)功能。As 直方图功能制作面元并计算每个面元中的点数；该函数计算每个箱的值的总和、平均值、中值、计数或其他统计数据。

> **参数:**
> **arr:**【array _ like】输入待入库数组。
> **值:**【array _ like】要计算哪个属性。
> **统计:**统计计算{均值、计数、中值、和、函数}。默认是卑鄙的。
> **bin:**【int 或 scalars】如果 bin 为 int，则定义给定范围内等宽 bin 的数量(默认为 10)。如果面元是一个序列，它定义面元的边。
> **范围:**(浮动，浮动)箱柜的上下范围，如果没有提供，范围从 x.max()到 x.min()。
> 
> **结果:**各仓统计值；箱边缘；箱号。

**代码#1 :**

```
# stats.binned_statistic() method 
import numpy as np
from scipy import stats

# 1D array
arr = [20, 2, 7, 1, 34]
print("\narr : \n", arr) 

# median  
print("\nbinned_statistic for median : \n", stats.binned_statistic(
        arr, np.arange(5), statistic ='median', bins = 4)) 
```

**输出:**

```
arr : 
 [20, 2, 7, 1, 34]

binned_statistic for median : 
 BinnedStatisticResult(statistic=array([ 2., nan,  0.,  4.]), 
bin_edges=array([ 1.,  9.25, 17.5, 25.75, 34\.  ]), 
binnumber=array([3, 1, 1, 1, 4], dtype=int64))

```

**代码#2 :**

```
# stats.binned_statistic() method 
import numpy as np
from scipy import stats

# mean  
arr = [20, 2, 7, 1, 34]
print("\nbinned_statistic for mean : \n", stats.binned_statistic(
        arr, np.arange(5), statistic ='mean', bins = 2)) 
```

**输出:**

```
binned_statistic for mean : 
 BinnedStatisticResult(statistic=array([2., 2.]), 
bin_edges=array([ 1., 17.5, 34\. ]), 
binnumber=array([2, 1, 1, 1, 2], dtype=int64))
```
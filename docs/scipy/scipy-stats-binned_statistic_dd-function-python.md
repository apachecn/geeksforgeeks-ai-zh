# sciPy stats . binned _ statistics _ DD()函数| Python

> 原文:[https://www . geesforgeks . org/scipy-stats-binned _ statistics _ DD-function-python/](https://www.geeksforgeeks.org/scipy-stats-binned_statistic_dd-function-python/)

`**stats.binned_statistic_dd(arr, values, statistic='mean', bins=10, range=None)**`函数计算给定二维数据的入库统计值。
工作原理类似于组织图 2d。As 直方图功能制作面元并计算每个面元中的点数；该函数计算每个箱的值的总和、平均值、中值、计数或其他统计数据。

> **参数:**
> **arr :** 【数组类】数据以(N，D)数组
> **的形式传递给直方图，值:**【数组类】用于计算统计数据。
> **统计:**统计计算{均值、计数、中值、和、函数}。默认是卑鄙的。
> **bin:**【int 或 scalars】如果 bin 为 int，则定义给定范围内等宽 bin 的数量(默认为 10)。如果面元是一个序列，它定义面元的边。
> **范围:**(浮动，浮动)箱柜的上下范围，如果没有提供，范围从 x.max()到 x.min()。
> 
> **结果:**各仓统计值；箱边缘；箱号。

**代码#1 :**

```py
# stats.binned_statistic_dd() method 
import numpy as np
from scipy import stats

x = np.ones(10)
y = np.ones(10)

print ("x : \n", x)
print ("\ny : \n", y)

print ("\nbinned_statistic_2d for count : ", 
       stats.binned_statistic_dd([x, y], None, 'count', bins = 3))
```

**输出:**

> x:
> 【1。1.1.1.1.1.1.1.1.1.]
> 
> y:
> 【1。1.1.1.1.1.1.1.1.1.]
> 
> 计数的 binned _ statistics _ 2d:BinnedStatisticddResult(statistics = array([[0。, 0., 0.】、
> 【0。, 10., 0.】、
> 【0。, 0., 0.])、bin_edges=[array([0.5，0.833333333，1.1666667，1.5 ])、
> array([0.5，0.833333333，1.16666667，1.5 ])、
> binnumber=array([12，12，12，12，12，12，12，12，12，12，12]，dtype = int64

**代码#2 :**

```py
# importing libraries
import numpy as np
from scipy import stats

# using np.ones for x and y
x = np.ones(10)
y = np.ones(10)

# Using binned_statistic_dd
print ("\nbinned_statistic_2d for count : ", 
        stats.binned_statistic_dd([x, y], None,
        'count', bins=3, range=[[2,3],[0,0.5]]))
```

**输出:**

> 计数的 binned _ statistics _ 2d:BinnedStatisticddResult(statistics = array([[0。, 0., 0.】、
> 【0。, 0., 0.】、
> 【0。, 0., 0.])，bin_edges=[array([2。, 2.33333333, 2.66666667, 3.])，
> 阵([0。，0.16666667，0.33333333，0.5 ])、
> binnumber=array([4，4，4，4，4，4，4，4，4，4，4，4，4]，dtype=int64))
# sciPy stats.bayes_mvs()函数| Python

> 原文:[https://www . geesforgeks . org/scipy-stats-Bayes _ MVS-function-python/](https://www.geeksforgeeks.org/scipy-stats-bayes_mvs-function-python/)

**scipy.stats.bayes_mvs(arr，alpha)** 函数计算给定贝叶斯置信区间内的均值、方差和标准差。

> **参数:**
> **arr:**【array _ like】输入数据可以是多维的，但使用前会被展平。
> **α:**返回的置信区间包含真参数的概率。
> 
> **结果:**给定贝叶斯置信区间内的均值、方差和标准差。

**代码#1:** 工作

```
# stats.bayes_mvs() method   
import numpy as np
from scipy import stats

arr1 = [[20, 2, 7, 1, 34],
        [50, 12, 12, 34, 4]]

arr2 = [50, 12, 12, 34, 4]

print ("\narr1 : ", arr1)
print ("\narr2 : ", arr2)

mean, var, std = stats.bayes_mvs(arr1, 0.9)

print ("\nMean of array1 : ", mean)
print ("\nvar of array1 : ", var)
print ("\nstd of array1 : ", std)

mean, var, std = stats.bayes_mvs(arr2, 0.5)

print ("\nMean of array2 : ", mean)
print ("\nvar of array2 : ", var)
print ("\nstd of array2 : ", std)

```

**输出:**

> arr1 : [[20，2，7，1，34]，[50，12，12，34，4]]
> 
> arr2 : [50，12，12，34，4]
> 
> 数组的平均值 1:平均值(统计量=17.6，最小最大值=(7.9921252273964，27))5888 . 88888888886
> 
> 数组的 var 1:方差(统计量=353.2，最小最大值=(146.176149159307
> 
> 数组 1 的标准值:Std_dev(统计值=18.136411760663574，minmax =(12.08849707316974，27.27))
> 
> 排列的平均值 2:平均值(统计量=22.4，最小最大值=(16.09058241339323，28.09660674004
> 
> 数组的 var 2:方差(统计量=725.6，最小最大值=(269 . 58888888881
> 
> 数组 2 的 Std:Std _ dev(统计值=23.872262300862655，minmax=(16.415719844632576，27.4150029646)
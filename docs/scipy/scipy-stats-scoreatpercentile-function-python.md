# sciPy stats . scoratpercentile()函数| Python

> 原文:[https://www . geeksforgeeks . org/scipy-stats-scoratpercentile-function-python/](https://www.geeksforgeeks.org/scipy-stats-scoreatpercentile-function-python/)

`**scipy.stats.scoreatpercentile(a, score, kind='rank')**`函数帮助我们计算输入数组给定百分位的得分。

百分位数= 50 的分数是中位数。如果期望的分位数位于两个数据点之间，我们根据插值的值在它们之间进行插值。

> **参数:**
> **arr:**【array _ like】输入数组。
> **per:**【array _ like】我们需要分数的百分位数。
> **极限:**【元组】计算百分位数的下限和上限。
> **轴:**【int】轴，我们需要沿着这个轴计算分数。
> 
> **结果:**相对于数组元素的百分位得分。

**代码#1:**

```py
# scoreatpercentile
from scipy import stats
import numpy as np 

# 1D array  
arr = [20, 2, 7, 1, 7, 7, 34, 3]

print("arr : ", arr)  

print ("\nScore at 50th percentile : ", 
       stats.scoreatpercentile(arr, 50))

print ("\nScore at 90th percentile : ", 
       stats.scoreatpercentile(arr, 90))

print ("\nScore at 10th percentile : ", 
       stats.scoreatpercentile(arr, 10))

print ("\nScore at 100th percentile : ", 
       stats.scoreatpercentile(arr, 100))

print ("\nScore at 30th percentile : ", 
       stats.scoreatpercentile(arr, 30))
```

**Output:**

```py
arr :  [20, 2, 7, 1, 7, 7, 34, 3]

Score at 50th percentile :  7.0

Score at 90th percentile :  24.2

Score at 10th percentile :  1.7

Score at 100th percentile :  34.0

Score at 30th percentile :  3.4

```

**代码#2:**

```py
# scoreatpercentile
from scipy import stats
import numpy as np 

arr = [[14, 17, 12, 33, 44],   
       [15, 6, 27, 8, 19],  
       [23, 2, 54, 1, 4, ]] 

print("arr : ", arr)  

print ("\nScore at 50th percentile : ", 
       stats.scoreatpercentile(arr, 50))

print ("\nScore at 50th percentile : ", 
       stats.scoreatpercentile(arr, 50, axis = 1))

print ("\nScore at 50th percentile : ", 
       stats.scoreatpercentile(arr, 50, axis = 0))
```

**Output:**

```py
arr :  [[14, 17, 12, 33, 44], [15, 6, 27, 8, 19], [23, 2, 54, 1, 4]]

Score at 50th percentile :  15.0

Score at 50th percentile :  [ 17\.  15\.   4.]

Score at 50th percentile :  [ 15\.   6\.  27\.   8\.  19.]

```
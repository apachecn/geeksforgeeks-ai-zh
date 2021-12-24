# sciPy stats . obrienttransform()函数| Python

> 原文:[https://www . geesforgeks . org/scipy-stats-obrientrant-function-python/](https://www.geeksforgeeks.org/scipy-stats-obrientransform-function-python/)

**scipy . stats . obrientrant(array)**函数计算给定数据上的**奥布莱恩变换**。使用奥布莱恩测试的主要思想是原始分数的转换，以便转换后的分数可以反映原始分数的变化。然后，对该转换后的分数进行方差分析，将得出原始分数的可变性(即方差)的差异，因此该分析将测试方差假设的同质性。

**其公式:**
![](img/024a07b031863a9af052de4e6d45594e.png)

```
N   = Number of observations
Ma  = Mean of the observations 
SSa = Sum of the squares of observations

```

> **参数:**
> **阵:**【阵样】阵数
> 
> **结果:**奥布莱恩变换的数组

**代码#1:** 工作

```
# stats.obrientransform() method   
import numpy as np
from scipy import stats

arr1 = [20, 2, 7, 1, 34]
arr2 = [50, 12, 12, 34, 4]

print ("arr1 : ", arr1)
print ("\narr2 : ", arr2)

print("\n O Brien Transform : \n", stats.obrientransform(arr1, arr2)) 

transform_arr1, transform_arr2 = stats.obrientransform(arr1, arr2)

print("\n O Brien Transform of arr1: \n", transform_arr1) 
print("\n O Brien Transform of arr2: \n", transform_arr2) 
```

**输出:**

> arr1 : [20，2，7，1，34]
> 
> arr2 : [50，12，12，34，4]
> 
> 奥布莱恩变换:
> 【【42.65 137.15 16.1083333 170.1083333 622.4833333】
> 【1050.43333333 97.2666667135.76666667】】
> 
> arr1 的奥布莱恩变换:
> 【42.65 137.15 16.1083333170.10833333622】
> 
> arr2 的奥布莱恩变换:
> [1050.4333333397 . 266666797 . 266667135 . 7666667433]
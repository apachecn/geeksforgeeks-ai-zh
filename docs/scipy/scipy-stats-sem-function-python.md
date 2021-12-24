# sciPy stats.sem()函数| Python

> 原文:[https://www . geesforgeks . org/scipy-stats-SEM-function-python/](https://www.geeksforgeeks.org/scipy-stats-sem-function-python/)

**scipy.stats.sem(arr，axis=0，ddof=0)** 函数用于计算输入数据平均值的标准误差。

> **参数:**
> **arr:**【array _ like】输入具有计算标准误差的元素的数组或对象。
> **轴:**计算平均值的轴。默认情况下，轴= 0。
> **ddof :** 标准差的自由度修正。
> 
> **结果:**输入数据平均值的标准误差。

**示例:**

```
# stats.sem() method 
import numpy as np
from scipy import stats

arr1 = [[20, 2, 7, 1, 34],
        [50, 12, 12, 34, 4]]

arr2 = [50, 12, 12, 34, 4]

print ("\narr1 : ", arr1)
print ("\narr2 : ", arr2)

print ("\nsem ratio for arr1 : ", 
       stats.sem(arr1, axis = 0, ddof = 0))

print ("\nsem ratio for arr1 : ", 
       stats.sem(arr1, axis = 1, ddof = 0))

print ("\nsem ratio for arr1 : ", 
       stats.sem(arr2, axis = 0, ddof = 0)) 
```

**输出:**

```
arr1 :  [[20, 2, 7, 1, 34], [50, 12, 12, 34, 4]]

arr2 :  [50, 12, 12, 34, 4]

sem ratio for arr1 :  [10.60660172  3.53553391  1.76776695 11.66726189 10.60660172]

sem ratio for arr1 :  [5.62423328 7.61892381]

sem ratio for arr1 :  7.618923808517841
```
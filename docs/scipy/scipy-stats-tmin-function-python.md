# scipy stats.tmin()函数| Python

> 原文:[https://www . geesforgeks . org/scipy-stats-tmin-function-python/](https://www.geeksforgeeks.org/scipy-stats-tmin-function-python/)

`**scipy.stats.tmin(array, lowerlimit=None, axis=0, inclusive=True)**` 函数沿指定轴计算数组元素的修剪最小值，同时忽略指定限制之外的值。

> **参数:**
> **数组:**输入数组或对象中具有计算最小值的元素。
> **轴:**【默认值为零】输入包含要计算最小值的元素的数组或对象。
> **限值:**数组的下限和上限要考虑，小于下限或大于上限的值将被忽略。如果限制为无[默认值]，则使用所有值。
> **包含:**决定是包含等于下限还是上限的值，还是在计算时将其排除。
> 
> **根据设定的参数返回:**数组元素的几何平均值。

**代码#1:**

```
# Trimmed Minimum 

from scipy import stats
import numpy as np 

# array elements ranging from 0 to 19
x = [1, 3, 27, 56, 2, 4, 13, 3, 6]

print("Trimmed Minimum :", stats.tmin(x)) 

print("\nTrimmed Minimum by setting limit : ", 
      stats.tmin(x, (5)))
```

**Output:**

```
Trimmed Minimum : 1

Trimmed Minimum by setting limit :  6

```

**代码#2:** 检查不同参数

```
# Trimmed Minimum 

from scipy import stats
import numpy as np 

# array elements ranging from 0 to 19
x = [[1, 3, 27], 
     [3, 4, 7], 
     [7, 6, 3], 
     [3, 6, 8]]

print("Trimmed Minimum :", stats.tmin(x)) 

# setting axis
print("\nTrimmed Minimum by setting axis : ", 
      stats.tmin(x, axis = 1))

print("\nTrimmed Minimum by setting axis : ", 
      stats.tmin(x, axis = 0))

# setting limit
print("\nTrimmed Minimum by setting limit : ", 
      stats.tmin(x, (5), axis = 1))

print("\nTrimmed Minimum by setting limit : ", 
      stats.tmin(x, (5), axis = 0))
```

**Output:**

```
Trimmed Minimum : [1 3 3]

Trimmed Minimum by setting axis :  [1 3 3 3]

Trimmed Minimum by setting axis :  [1 3 3]

Trimmed Minimum by setting limit :  [27  7  6  6]

Trimmed Minimum by setting limit :  [7 6 7]

```
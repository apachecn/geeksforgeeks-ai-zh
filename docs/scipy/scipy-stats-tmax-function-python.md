# sciPy stats.tmax()函数| Python

> 原文:[https://www . geesforgeks . org/scipy-stats-tmax-function-python/](https://www.geeksforgeeks.org/scipy-stats-tmax-function-python/)

`**scipy.stats.tmax(array, lowerlimit=None, axis=0, inclusive=True)**`函数沿指定轴计算数组元素的修剪最大值，同时忽略指定限制之外的值。

> **参数:**
> **数组:**输入数组或对象中具有计算修剪后最大值的元素。
> **轴:**轴，统计数据将沿着该轴计算。默认轴= 0
> **限制:**考虑数组的下限和上限，小于下限或大于上限的值将被忽略。如果限制为无[默认值]，则使用所有值。
> **包含:**决定是包含等于下限还是上限的值，还是在计算时将其排除。
> 
> **返回:**根据设置的参数，修剪数组元素的最大值。

**代码#1:**

```
# Trimmed Maximum 

from scipy import stats
import numpy as np 

# array elements ranging from 0 to 19
x = [1, 3, 27, 56, 2, 4, 13, 3, 6]

print("Trimmed Maximum :", stats.tmax(x)) 

print("\nTrimmed Maximum by setting limit : ", 
      stats.tmax(x, (5)))
```

**Output:**

```
Trimmed Maximum : 56

Trimmed Maximum by setting limit :  4

```

**代码#2:** 多维数据

```
# Trimmed Maximum 

from scipy import stats
import numpy as np 

# array elements ranging from 0 to 19
x = [[1, 3, 27], 
        [3, 4, 7], 
        [7, 6, 3], 
        [3, 6, 8]]

print("Trimmed Maximum :", stats.tmax(x)) 

# setting axis
print("\nTrimmed Maximum by setting axis : ", 
      stats.tmax(x, axis = 1))

print("\nTrimmed Maximum by setting axis : ", 
      stats.tmax(x, axis = 0))

# setting limit
print("\nTrimmed Maximum by setting limit : ", 
      stats.tmax(x, (5), axis = 1))

print("\nTrimmed Maximum by setting limit : ", 
      stats.tmax(x, (5), axis = 0))
```

**Output:**

```
Trimmed Maximum : [ 7  6 27]

Trimmed Maximum by setting axis :  [27  7  7  8]

Trimmed Maximum by setting axis :  [ 7  6 27]

Trimmed Maximum by setting limit :  [3 4 3 3]

Trimmed Maximum by setting limit :  [3 4 3]

```
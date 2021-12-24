# sciPy stats.tstd()函数| Python

> 原文:[https://www . geesforgeks . org/scipy-stats-tstd-function-python/](https://www.geeksforgeeks.org/scipy-stats-tstd-function-python/)

**`scipy.stats.tstd(array, limits=None, inclusive=(True, True))`** 计算数组元素沿数组指定轴的修剪标准差。

是公式–
![](img/8e951e6c0f6eed705659cc9109ba3d6e.png)

> **参数:**
> **数组:**输入数组或具有计算修剪标准差元素的对象。
> **轴:**轴，沿该轴计算修剪后的标准偏差。默认情况下，轴= 0。
> **限值:**数组的下限和上限要考虑，小于下限或大于上限的值将被忽略。如果限制为无[默认值]，则使用所有值。
> 
> **返回:**根据设置的参数对数组元素的标准偏差进行修剪。

**代码#1:**

```py
# Trimmed Standard Deviation 

from scipy import stats
import numpy as np 

# array elements ranging from 0 to 19
x = np.arange(20)

print("Trimmed Standard Deviation :", stats.tstd(x)) 

print("\nTrimmed Standard Deviation by setting limit : ", 
      stats.tstd(x, (2, 10)))
```

**Output:**

```py
Trimmed Standard Deviation : 5.9160797831

Trimmed Standard Deviation by setting limit :  2.73861278753

```

**代码#2:** 多维数据，轴()工作

```py
# Trimmed Standard Deviation 

from scipy import stats
import numpy as np 

arr1 = [[1, 3, 27], 
        [5, 3, 18], 
        [17, 16, 333], 
        [3, 6, 82]] 

# using axis = 0
print("Trimmed Standard Deviation is with default axis = 0 : \n", 
      stats.tstd(arr1, axis = 1))
```

**Output:**

```py
Trimmed Standard Deviation is with default axis = 0 : 
 94.0423824505

```
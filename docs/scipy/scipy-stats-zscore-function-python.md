# sciPy stats.zscore()函数| Python

> 原文:[https://www . geesforgeks . org/scipy-stats-zs core-function-python/](https://www.geeksforgeeks.org/scipy-stats-zscore-function-python/)

**scipy.stats.zscore(arr，axis=0，ddof=0)** 函数计算输入数据相对于样本平均值和标准偏差的相对 **Z 分数**。

**其公式:**
![](img/24720b169e1be0c14d7f8900f3035ebb.png)

> **参数:**
> **arr :** 【类数组】输入要计算 Z 分数的数组或对象。
> **轴:**计算平均值的轴。默认情况下，轴= 0。
> **ddof :** 标准差的自由度修正。
> 
> **结果:**输入数据的 Z 评分。

**代码#1:工作**

```
# stats.zscore() method  
import numpy as np
from scipy import stats

arr1 = [[20, 2, 7, 1, 34],
        [50, 12, 12, 34, 4]]

arr2 = [[50, 12, 12, 34, 4], 
        [12, 11, 10, 34, 21]]

print ("\narr1 : ", arr1)
print ("\narr2 : ", arr2)

print ("\nZ-score for arr1 : \n", stats.zscore(arr1))
print ("\nZ-score for arr1 : \n", stats.zscore(arr1, axis = 1))
```

**输出:**

```
arr1 :  [[20, 2, 7, 1, 34], [50, 12, 12, 34, 4]]

arr2 :  [[50, 12, 12, 34, 4], [12, 11, 10, 34, 21]]

Z-score for arr1 : 
 [[-1\. -1\. -1\. -1\.  1.]
 [ 1\.  1\.  1\.  1\. -1.]]

Z-score for arr1 : 
 [[ 0.57251144 -0.85876716 -0.46118977 -0.93828264  1.68572813]
 [ 1.62005758 -0.61045648 -0.61045648  0.68089376 -1.08003838]]

```

**代码#2 : Z 评分**

```
import numpy as np
from scipy import stats

arr2 = [[50, 12, 12, 34, 4], 
        [12, 11, 10, 34, 21]]

print ("\nZ-score for arr2 : \n", stats.zscore(arr2, axis = 0))
print ("\nZ-score for arr2 : \n", stats.zscore(arr2, axis = 1))
```

**输出:**

```

Z-score for arr2 : 
 [[ 1\.  1\.  1\. nan -1.]
 [-1\. -1\. -1\. nan  1.]]

Z-score for arr2 : 
 [[ 1.62005758 -0.61045648 -0.61045648  0.68089376 -1.08003838]
 [-0.61601725 -0.72602033 -0.83602341  1.80405051  0.37401047]]

```
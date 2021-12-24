# sciPy stats.zmap()函数| Python

> 原文:[https://www . geesforgeks . org/scipy-stats-zmap-function-python/](https://www.geeksforgeeks.org/scipy-stats-zmap-function-python/)

**scipy.stats.zmap(scores，compare，axis=0，ddof=0)** 函数计算输入数据的相对 **Z 分数**。标准化为零均值和单位方差的分数，其中均值和方差是根据比较数组计算的。

**其公式:**
![](img/24720b169e1be0c14d7f8900f3035ebb.png)

> **参数:**
> **分数:**【array _ like】输入要计算 Z 分数的数组或对象。
> **比较:**【array _ like】输入数组或对象，对其取归一化的平均值和标准偏差
> **轴:**计算平均值的轴。默认情况下，轴= 0。
> **ddof :** 标准差的自由度修正。
> 
> **结果:**输入数据的 Z 评分。

**代码#1:工作**

```
# stats.zmap() method   
import numpy as np
from scipy import stats

arr1 = [[20, 2, 7, 1, 34],
        [50, 12, 12, 34, 4]]

arr2 = [[50, 12, 12, 34, 4], 
        [12, 11, 10, 34, 21]]

print ("\narr1 : ", arr1)
print ("\narr2 : ", arr2)

print ("\nZ-score : \n", stats.zmap(arr1, arr2))
```

**输出:**

```
arr1 :  [[20, 2, 7, 1, 34], [50, 12, 12, 34, 4]]

arr2 :  [[50, 12, 12, 34, 4], [12, 11, 10, 34, 21]]

Z-score : 
 [[ -0.57894737 -19\.          -4\.                 -inf   2.52941176]
 [  1\.           1\.           1\.                  nan  -1\.        ]]

```

**代码#2 : Z 评分**

```
# stats.zmap() method   
import numpy as np
from scipy import stats

arr1 = [[20, 2, 7, 1, 34],
        [50, 12, 12, 34, 4]]

arr2 = [[50, 12, 12, 34, 4], 
        [12, 11, 10, 34, 21]]

print ("\nZ-score : \n", stats.zmap(arr1, arr2, axis = 1))
```

**输出:**

```
sem ratio for arr1 : 
 [[-0.14087457 -1.19743386 -0.90394517 -1.2561316   0.68089376]
 [ 3.5640998  -0.61601725 -0.61601725  1.80405051 -1.49604189]]

```
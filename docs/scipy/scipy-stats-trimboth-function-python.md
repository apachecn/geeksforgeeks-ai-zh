# sciPy stats.trimboth()函数| Python

> 原文:[https://www . geeksforgeeks . org/scipy-stats-trimboth-function-python/](https://www.geeksforgeeks.org/scipy-stats-trimboth-function-python/)

**scipy.stats.trimboth(a，proportiontocut，axis=0)** 函数从数组的两端切掉数组中的部分元素。

> **参数:**
> **arr:**【array _ like】输入要修剪的数组或对象。
> **轴:**计算平均值的轴。默认情况下，轴= 0。
> **比例分配:**每端要修剪的数据比例(在 0-1 范围内)。
> 
> **结果:**按照给定的比例从两端修剪数组元素。

**代码#1:工作**

```
# stats.trimboth() method   
import numpy as np
from scipy import stats

arr1 = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

print ("\narr1 : ", arr1)

print ("\nclipped arr1 : \n", stats.trimboth(arr1, proportiontocut = .3))
print ("\nclipped arr1 : \n", stats.trimboth(arr1, proportiontocut = .1))
```

**输出:**

```
arr1 :  [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

clipped arr1 : 
 [3 4 5 6]

clipped arr1 : 
 [1 3 2 4 5 6 7 8]

```

**代码#2:**

```
# stats.trimboth() method   
import numpy as np
from scipy import stats

arr1 = [[0, 12, 21, 3, 14],
        [53, 16, 37, 85, 39]]

print ("\narr1 : ", arr1)

print ("\nclipped arr1 : \n", 
       stats.trimboth(arr1, proportiontocut = .3))

print ("\nclipped arr1 : \n", 
       stats.trimboth(arr1, proportiontocut = .1))

print ("\nclipped arr1 : \n", 
       stats.trimboth(arr1, proportiontocut = .1, axis = 1))

print ("\nclipped arr1 : \n", 
       stats.trimboth(arr1, proportiontocut = .1, axis = 0))
```

**输出:**

```
arr1 :  [[0, 12, 21, 3, 14], [53, 16, 37, 85, 39]]

clipped arr1 : 
 [[ 0 12 21  3 14]
 [53 16 37 85 39]]

clipped arr1 : 
 [[ 0 12 21  3 14]
 [53 16 37 85 39]]

clipped arr1 : 
 [[ 0  3 12 14 21]
 [16 37 39 53 85]]

clipped arr1 : 
 [[ 0 12 21  3 14]
 [53 16 37 85 39]]

```
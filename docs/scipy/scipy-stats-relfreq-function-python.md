# sciPy stats.relfreq()函数| Python

> 原文:[https://www . geesforgeks . org/scipy-stats-relfreq-function-python/](https://www.geeksforgeeks.org/scipy-stats-relfreq-function-python/)

`**scipy.stats.relfreq(a, numbins, defaultreallimits, weights)**`是相对频率直方图，使用直方图函数。

> **参数:**
> **arr:**【array _ like】输入数组。
> **numbins :** 直方图使用的箱数。[Default = 10]
> **Default real limits:**(下限，上限)直方图的范围。
> **权重:**【array _ like】每个数组元素的权重。
> 
> **结果:**
> –相对频率箱值
> –每个箱的宽度
> –实际下限
> –加分。

**代码#1:**

```py
# relative frequency
from scipy import stats
import numpy as np 

arr1 = [1, 3, 27, 2, 5, 13] 
print ("Array element : ", arr1, "\n")

a, b, c, d = stats.relfreq(arr1, numbins = 4)

print ("cumulative frequency : ", a)
print ("Lower Limit : ", b)
print ("bin size : ", c)
print ("extra-points : ", d)
```

**输出:**

```py
Array element :  [1, 3, 27, 2, 5, 13] 

cumulative frequency :  [0.66666667 0.16666667 0\.         0.16666667]
Lower Limit :  -3.333333333333333
bin size :  8.666666666666666
extra-points :  0

```

**代码#2:**

```py
# relative frequency
from scipy import stats
import numpy as np 

arr1 = [1, 3, 27, 2, 5, 13] 
print ("Array element : ", arr1, "\n")

a, b, c, d = stats.relfreq(arr1, numbins = 4,
              weights = [.1, .2, .1, .3, 1, 6])

print ("cumfreqs : ", a)
print ("lowlim : ", b)
print ("binsize : ", c)
print ("extrapoints : ", d)
```

**输出:**

```py
Array element :  [1, 3, 27, 2, 5, 13] 

cumfreqs :  [0.26666667 1\.         0\.         0.01666667]
lowlim :  -3.333333333333333
binsize :  8.666666666666666
extrapoints :  0
```
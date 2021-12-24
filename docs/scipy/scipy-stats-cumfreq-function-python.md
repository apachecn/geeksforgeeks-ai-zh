# sciPy stats.cumfreq()函数| Python

> 原文:[https://www . geesforgeks . org/scipy-stats-cumfreq-function-python/](https://www.geeksforgeeks.org/scipy-stats-cumfreq-function-python/)

**scipy.stats.cumfreq(a，numbins，defaultreallimits，weights)** 使用直方图函数工作，并计算累积频率直方图。它包括累计频率箱值、每个箱的宽度、实际下限、额外点数。

> **参数:**
> **arr:**【array _ like】输入数组。
> **numbins:**【int】直方图使用的箱数。[Default = 10]
> **Default limits:**(下限，上限)直方图的范围。
> **权重:**【array _ like】每个数组元素的权重。
> **结果:**
> –累计频率入库值
> –各仓宽度
> –实下限
> –加分。

**代码#1:**

## 蟒蛇 3

```
# cumulative frequency
from scipy import stats
import numpy as np 

arr1 = [1, 3, 27, 2, 5, 13] 
print ("Array element : ", arr1, "\n")

a, b, c, d = stats.cumfreq(arr1, numbins = 4)

print ("cumulative frequency : ", a)
print ("Lower Limit : ", b)
print ("bin size : ", c)
print ("extra-points : ", d)
```

**Output:** 

```
Array element :  [1, 3, 27, 2, 5, 13] 

cumulative frequency :  [ 4\.  5\.  5\.  6.]
Lower Limit :  -3.33333333333
bin size :  8.66666666667
extra-points :  0
```

**代码#2:**

## 蟒蛇 3

```
# cummulative frequency
from scipy import stats
import numpy as np 

arr1 = [1, 3, 27, 2, 5, 13] 
print ("Array element : ", arr1, "\n")

a, b, c, d = stats.cumfreq(arr1, numbins = 4,
              weights = [.1, .2, .1, .3, 1, 6])

print ("cumfreqs : ", a)
print ("lowlim : ", b)
print ("binsize : ", c)
print ("extrapoints : ", d)
```

**Output:** 

```
Array element :  [1, 3, 27, 2, 5, 13] 

cumfreqs :  [ 1.6  7.6  7.6  7.7]
lowlim :  -3.33333333333
binsize :  8.66666666667
extrapoints :  0
```
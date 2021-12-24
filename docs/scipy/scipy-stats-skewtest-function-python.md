# scipy stats.skewtest()函数| Python

> 原文:[https://www . geesforgeks . org/scipy-stats-skew test-function-python/](https://www.geeksforgeeks.org/scipy-stats-skewtest-function-python/)

`**scipy.stats.skewtest(array, axis=0)**`功能测试歪斜是否不同于正态分布。这个函数检验零假设，即抽样的总体偏度与相应正态分布的偏度相同。

**其公式–**
![](img/8f05ec50d85b90b45acc7e42ad84dfb4.png)

> **参数:**
> **数组:**输入数组或有元素的对象。
> **轴:**轴，偏斜度测试将沿着该轴计算。默认情况下，轴= 0。
> 
> **返回:**数据集假设检验的 Z 值(统计值)和 P 值。

**代码#1:**

```py
# Performing skewtest
from scipy.stats import skewtest
import numpy as np 
import pylab as p 

x1 = np.linspace( -5, 5, 1000 )
y1 = 1./(np.sqrt(2.*np.pi)) * np.exp( -.5*(x1)**2  )

p.plot(x1, y1, '*')

print( '\nSkewness test for given data :\n', skewtest(y1))
```

**输出:**

```py

Skewness test for given data :
 SkewtestResult(statistic=11.874007880556805, pvalue=1.6153913086650964e-32)

```

**代码#2:**

```py
# Performing skewtest
from scipy.stats import skewtest
import numpy as np 
import pylab as p 

x1 = np.linspace( -5, 12, 1000 )
y1 = 1./(np.sqrt(2.*np.pi)) * np.exp( -.5*(x1)**2  )

p.plot(x1, y1, '.')

print( '\nSkewness for data :\n', skewtest(y1))
```

**输出:**

```py

Skewness for data :
 SkewtestResult(statistic=16.957642860709516, pvalue=1.689888374767126e-64)

```
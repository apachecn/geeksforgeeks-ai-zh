# scipy stats . kurtositest()函数| Python

> 原文:[https://www . geeksforgeeks . org/scipy-stats-kurtosist-function-python/](https://www.geeksforgeeks.org/scipy-stats-kurtosistest-function-python/)

`**scipy.stats.kurtosistest(array, axis=0)**`函数检验给定数据集是否具有正态峰度(Fisher 或 Pearson)。

**什么是峰度？**
是第四个中心矩除以方差的平方。它是“尾部”的度量，即实值随机变量概率分布的形状描述符。简单来说，可以说它是衡量尾部相对于正态分布有多重的标准。

**其公式–**
![](img/cdebbf3fc491ab19372c94a9446abb4c.png)

> **参数:**
> **数组:**输入数组或有元素的对象。
> **轴:**轴，将沿该轴计算 kurtosistest。默认情况下，轴= 0。
> 
> **返回:**正态分布数据集的 Z 值(统计值)和 P 值。

**代码#1:**

```py
# Graph using numpy.linspace() 
# finding kurtosis

from scipy.stats import kurtosistest
import numpy as np 
import pylab as p 

x1 = np.linspace( -5, 5, 1000 )
y1 = 1./(np.sqrt(2.*np.pi)) * np.exp( -.5*(x1)**2  )

p.plot(x1, y1, '*')

print( '\nKurtosis for normal distribution :\n', kurtosistest(y1))
```

**输出:**

```py

Kurtosis for normal distribution :
 KurtosistestResult(statistic=-2.2557936070461615, pvalue=0.024083559905734513)

```
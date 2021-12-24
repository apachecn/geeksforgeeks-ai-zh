# scipy stats .峰度()函数| Python

> 原文:[https://www . geeksforgeeks . org/scipy-stats-峰度-function-python/](https://www.geeksforgeeks.org/scipy-stats-kurtosis-function-python/)

`**scipy.stats.kurtosis(array, axis=0, fisher=True, bias=True)**`函数计算数据集的峰度(Fisher 或 Pearson)。它是第四个中心矩除以方差的平方。它是“尾部”的度量，即实值随机变量概率分布的形状描述符。简单来说，可以说它是衡量尾部相对于正态分布有多重的标准。

**其公式–**
![](img/cdebbf3fc491ab19372c94a9446abb4c.png)

> **参数:**
> **数组:**输入数组或有元素的对象。
> **轴:**测量峰度值的轴。默认情况下，轴= 0。
> **费希尔:**Bool；如果为真，则使用费希尔定义(正常 0.0)；否则，如果设置为 False，将使用 Pearson 的定义(normal 3.0)。
> **偏向:**Bool；如果设置为假，计算将针对统计偏差进行校正。
> 
> **返回:**数据集正态分布的峰度值。

**代码#1:**

```
# Graph using numpy.linspace() 
# finding kurtosis

from scipy.stats import kurtosis
import numpy as np 
import pylab as p 

x1 = np.linspace( -5, 5, 1000 )
y1 = 1./(np.sqrt(2.*np.pi)) * np.exp( -.5*(x1)**2  )

p.plot(x1, y1, '*')

print( '\nKurtosis for normal distribution :', kurtosis(y1))

print( '\nKurtosis for normal distribution :', 
      kurtosis(y1, fisher = False))

print( '\nKurtosis for normal distribution :', 
      kurtosis(y1, fisher = True))
```

**输出:**

```

Kurtosis for normal distribution : -0.3073930877422071

Kurtosis for normal distribution : 2.692606912257793

Kurtosis for normal distribution : -0.3073930877422071

```
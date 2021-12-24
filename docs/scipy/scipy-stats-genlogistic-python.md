# scipy stats . genlogistic()| Python

> 原文:[https://www . geesforgeks . org/scipy-stats-gen logistic-python/](https://www.geeksforgeeks.org/scipy-stats-genlogistic-python/)

**scipy . stats . gen logistic()**是一个广义 logistic 连续随机变量，用标准格式和一些形状参数来定义，以完成其规格。
T3】

> **参数:**
> **- > q :** 上下尾概率
> **- > a、b :** 形状参数
> **- > x :** 分位数
> **- > loc :** 【可选】位置参数。默认= 0
> **- >刻度:**【可选】刻度参数。默认值= 1
> **- >大小:**【整数元组，可选】形状或随机变量。
> **- >矩:**【可选】由字母['mvsk']组成；m’=均值，‘v’=方差，‘s’= Fisher 偏斜度，‘k’= Fisher 峰度。(默认值= 'mv ')。
> 
> **结果:**广义 logistic 连续随机变量

**代码#1:创建广义逻辑连续随机变量**

```
from scipy.stats import genlogistic 

numargs = genlogistic .numargs
[a] = [0.7, ] * numargs
rv = genlogistic (a)

print ("RV : \n", rv) 
```

**输出:**

```
RV : 
 <scipy.stats._distn_infrastructure.rv_frozen object at 0x0000018D578F4D30>

```

**代码#2:广义逻辑随机变量和概率分布。**

```
import numpy as np
quantile = np.arange (0.01, 1, 0.1)

# Random Variates
R = genlogistic.rvs(a, scale = 2,  size = 10)
print ("Random Variates : \n", R)

# PDF
R = genlogistic.pdf(a, quantile, loc = 0, scale = 1)
print ("\nProbability Distribution : \n", R)
```

**输出:**

```
Random Variates : 
 [-2.25279702 -1.09146871 -0.01100363 -3.95860336  5.07952934 -2.3073455
 -3.11698062 -0.32931819  8.84452349 -3.06546109]

Probability Distribution : 
 [0.00330477 0.03491595 0.06402364 0.09077633 0.11531469 0.13777195
 0.15827427 0.17694109 0.19388545 0.20921433]

```

**代码#3:图形表示。**

```
import numpy as np
import matplotlib.pyplot as plt

distribution = np.linspace(0, np.minimum(rv.dist.b, 3))
print("Distribution : \n", distribution)

plot = plt.plot(distribution, rv.pdf(distribution))
```

**输出:**

```
Distribution : 
 [0\.         0.06122449 0.12244898 0.18367347 0.24489796 0.30612245
 0.36734694 0.42857143 0.48979592 0.55102041 0.6122449  0.67346939
 0.73469388 0.79591837 0.85714286 0.91836735 0.97959184 1.04081633
 1.10204082 1.16326531 1.2244898  1.28571429 1.34693878 1.40816327
 1.46938776 1.53061224 1.59183673 1.65306122 1.71428571 1.7755102
 1.83673469 1.89795918 1.95918367 2.02040816 2.08163265 2.14285714
 2.20408163 2.26530612 2.32653061 2.3877551  2.44897959 2.51020408
 2.57142857 2.63265306 2.69387755 2.75510204 2.81632653 2.87755102
 2.93877551 3\.        ]
```

![](img/e34da44a235403e58edf8f7a027d5e52.png)

**代码#4:变化的位置参数**

```
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 5, 100)

# Varying positional arguments
y1 = genlogistic.pdf(x, 1, 3)
y2 = genlogistic.pdf(x, 1, 4)
plt.plot(x, y1, "*", x, y2, "r--")
```

**输出:**
![](img/07b34b777cc39e28b5da14dd5bb7ff4a.png)
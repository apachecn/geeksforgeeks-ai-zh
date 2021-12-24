# scipy stats . Bradford()| Python

> 原文:[https://www.geeksforgeeks.org/scipy-stats-bradford-python/](https://www.geeksforgeeks.org/scipy-stats-bradford-python/)

**scipy.stats.bradford()** 是一个 bradford 连续随机变量，用标准格式和一些形状参数定义，以完成其规格。

![](img/74ea361511331fe01b39cc9e4e9d4988.png)

> **参数:**
> **q :** 上下尾概率
> **x :** 分位数
> **loc :** 【可选】位置参数。默认= 0
> **比例:**【可选】比例参数。默认值= 1
> **大小:**【整数元组，可选】形状或随机变量。
> **瞬间:**【可选】由字母['mvsk']组成；m’=均值，‘v’=方差，‘s’= Fisher 偏斜度，‘k’= Fisher 峰度。(默认值= 'mv ')。
> 
> **结果:**布拉德福连续随机变量

**代码#1:创建布拉德福连续随机变量**

```
# importing scipy
from scipy.stats import bradford

numargs = bradford.numargs
[a] = [0.6, ] * numargs
rv = bradford(a)

print ("RV : \n", rv)
```

**输出:**

```
RV : 
 <scipy.stats._distn_infrastructure.rv_frozen object at 0x00000294853B04A8>

```

**代码#2 :** 布拉德福随机变量和概率分布

```
import numpy as np
quantile = np.arange (0.01, 1, 0.1)

# Random Variates
R = bradford.rvs(a, scale = 2,  size = 10)
print ("Random Variates : \n", R)

# PDF
R = bradford.pdf(quantile, a, loc = 0, scale = 1)
print ("\nProbability Distribution : \n", R)
```

**输出:**

```
Random Variates : 
 [0.30727583 0.22129839 0.27130072 0.19795865 1.66069665 1.93938843
 0.43435698 0.16437308 0.91592562 1.95369029]

Probability Distribution : 
 [1.26897205 1.19754774 1.13373525 1.07637933 1.02454726 0.97747771
 0.93454311 0.89522152 0.85907529 0.82573473]
```

**代码#3:图形表示。**

```
import numpy as np
import matplotlib.pyplot as plt

distribution = np.linspace(0, np.maximum(rv.dist.b, 5))
print ("Distribution : \n", distribution)

plot = plt.plot(distribution, rv.pdf(distribution))
```

**输出:**

```
Distribution : 
 [0\.         0.10204082 0.20408163 0.30612245 0.40816327 0.51020408
 0.6122449  0.71428571 0.81632653 0.91836735 1.02040816 1.12244898
 1.2244898  1.32653061 1.42857143 1.53061224 1.63265306 1.73469388
 1.83673469 1.93877551 2.04081633 2.14285714 2.24489796 2.34693878
 2.44897959 2.55102041 2.65306122 2.75510204 2.85714286 2.95918367
 3.06122449 3.16326531 3.26530612 3.36734694 3.46938776 3.57142857
 3.67346939 3.7755102  3.87755102 3.97959184 4.08163265 4.18367347
 4.28571429 4.3877551  4.48979592 4.59183673 4.69387755 4.79591837
 4.89795918 5\.        ]
```

![](img/498c929f9f3e6ea1467dc6d9764ff541.png)
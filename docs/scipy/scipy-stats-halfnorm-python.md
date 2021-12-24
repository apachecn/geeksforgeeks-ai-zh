# scipy stat . halform()\ python

> 原文:[https://www.geeksforgeeks.org/scipy-stats-halfnorm-python/](https://www.geeksforgeeks.org/scipy-stats-halfnorm-python/)

**scipy.stats.halfnorm()** 是一个半正态连续随机变量，用标准格式和一些形状参数来定义，以完成其规范。

![](img/a8fab82811639139372934f2ad5e5176.png)

> **参数:**
> **- > q :** 上下尾概率
> **- > x :** 分位数
> **- > loc :** 【可选】位置参数。默认= 0
> **- >刻度:**【可选】刻度参数。默认值= 1
> **- >大小:**【整数元组，可选】形状或随机变量。
> **- >瞬间:**【可选】由字母['mvsk']组成；m’=均值，‘v’=方差，‘s’= Fisher 偏斜度，‘k’= Fisher 峰度。(默认值= 'mv ')。
> 
> **结果:**半正态连续随机变量

**代码#1:创建半正态连续随机变量**

```py
from scipy.stats import halfnorm  

numargs = halfnorm.numargs
[] = [0.7, ] * numargs
rv = halfnorm()

print ("RV : \n", rv) 
```

**输出:**

```py
RV : 
 <scipy.stats._distn_infrastructure.rv_frozen object at 0x000001E39B53B630>

```

**代码#2:半正态随机变量和概率分布**

```py
import numpy as np
quantile = np.arange (0.01, 1, 0.1)

# Random Variates
R = halfnorm.rvs(scale = 2,  size = 10)
print ("Random Variates : \n", R)

# PDF
R = halfnorm.pdf(quantile, loc = 0, scale = 1)
print ("\nProbability Distribution : \n", R)
```

**输出:**

```py
Random Variates : 
 [3.95023511 1.97013912 2.00977927 1.88217027 2.24680027 0.7298033
 0.56769996 0.62071753 1.74743798 0.35512999]

Probability Distribution : 
 [0.79784467 0.79307193 0.78048376 0.76045271 0.73356332 0.70058376
 0.66242936 0.62012057 0.57473779 0.52737608]
```

**代码#3:图形表示。**

```py
import numpy as np
import matplotlib.pyplot as plt

distribution = np.linspace(0, np.minimum(rv.dist.b, 3))
print("Distribution : \n", distribution)

plot = plt.plot(distribution, rv.pdf(distribution))
```

**输出:**

```py
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

![](img/5ac516ae26ffd0cd0c3f3ab700d97830.png)

**代码#4:变化的位置参数**

```py
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 5, 100)

# Varying positional arguments
y1 = halfnorm.pdf(x, 1, 3)
y2 = halfnorm.pdf(x, 1, 4)
plt.plot(x, y1, "*", x, y2, "r--")
```

**输出:**
![](img/d9d55db5d2fbd9954aa7979ac19c7e82.png)
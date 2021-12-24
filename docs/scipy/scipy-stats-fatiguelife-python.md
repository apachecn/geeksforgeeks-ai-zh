# scipy stats .疲劳()| Python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/scipy-stats-tire fife-python/

**scipy . stats . default life()**是疲劳寿命(Birnbaum-Sanders)连续随机变量，用标准格式和一些形状参数定义，以完成其规格。
T3】

> **参数:**
> **q :** 上下尾概率
> **x :** 分位数
> **loc :** 【可选】位置参数。默认= 0
> **比例:**【可选】比例参数。默认值= 1
> **大小:**【整数元组，可选】形状或随机变量。
> **瞬间:**【可选】由字母['mvsk']组成；m’=均值，‘v’=方差，‘s’= Fisher 偏斜度，‘k’= Fisher 峰度。(默认值= 'mv ')。
> 
> **结果:**疲劳寿命(Birnbaum-Sanders)连续随机变量

**代码#1:创建疲劳寿命连续随机变量**

```
from scipy.stats import fatiguelife

numargs = fatiguelife.numargs
[a] = [0.7, ] * numargs
rv = fatiguelife(a)

print ("RV : \n", rv) 
```

**输出:**

```
RV : 
 <scipy.stats._distn_infrastructure.rv_frozen object at 0x0000018D567B8400>

```

**代码#2:疲劳寿命随机变量和概率分布。**

```
import numpy as np
quantile = np.arange (0.01, 1, 0.1)

# Random Variates
R = fatiguelife.rvs(a, scale = 2,  size = 10)
print ("Random Variates : \n", R)

# PDF
R = fatiguelife.pdf(a, quantile, loc = 0, scale = 1)
print ("\nProbability Distribution : \n", R)
```

**输出:**

```
Random Variates : 
 [ 1.5759368   1.73788302  2.31297609  1.0005871   1.49635022 11.98492239
  2.51785146  4.0096255   0.5654246   0.97502712]

Probability Distribution : 
 [3.74431292e-278 2.59381847e-002 6.41771315e-001 9.56754833e-001
 9.63413710e-001 8.86691481e-001 7.98585419e-001 7.17860186e-001
 6.48103032e-001 5.88743459e-001]

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

![](img/1732fad6857382ae6d406b94b8975807.png)

**代码#4:变化的位置参数**

```
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 5, 100)

# Varying positional arguments
y1 = fatiguelife.pdf(x, 1, 3)
y2 = fatiguelife.pdf(x, 1, 4)
plt.plot(x, y1, "*", x, y2, "r--")
```

**输出:**
![](img/6feccf43d4ef59043925f1f1591a4d2a.png)
# scipy stats . gilbrat()| python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/scipy-stats-gilbrat-python/

**scipy.stats.gilbrat()** 是一个 gilbrat 连续随机变量，用标准格式和一些形状参数定义，以完成其规范。

![](img/d719e42a72360e6f68cf2eeea858c9df.png)

> **参数:**
> **- > q :** 上下尾概率
> **- > x :** 分位数
> **- > loc :** 【可选】位置参数。默认= 0
> **- >刻度:**【可选】刻度参数。默认值= 1
> **- >大小:**【整数元组，可选】形状或随机变量。
> **- >瞬间:**【可选】由字母['mvsk']组成；m’=均值，‘v’=方差，‘s’= Fisher 偏斜度，‘k’= Fisher 峰度。(默认值= 'mv ')。
> 
> **结果:**吉尔布雷特连续随机变量

**代码#1:创建吉尔布雷特连续随机变量**

```
from scipy.stats import gilbrat 

numargs = gilbrat .numargs
[] = [0.7, ] * numargs
rv = gilbrat ()

print ("RV : \n", rv) 
```

**输出:**

```
RV : 
 <scipy.stats._distn_infrastructure.rv_frozen object at 0x000001E39A3B4AC8>

```

**代码#2:吉尔布雷特随机变量和概率分布**

```
import numpy as np
import numpy as np
quantile = np.arange (0.01, 1, 0.1)

# Random Variates
R = gilbrat.rvs(scale = 2,  size = 10)
print ("Random Variates : \n", R)

# PDF
R = gilbrat.pdf(quantile, loc = 0, scale = 1)
print ("\nProbability Distribution : \n", R)
```

**输出:**

```
Random Variates : 
 [0.66090031 1.39027118 1.33876164 1.50366592 5.21419497 5.24225463
 3.98547687 0.30586938 9.11346685 0.93014057]

Probability Distribution : 
 [0.00099024 0.31736749 0.5620854  0.64817773 0.65389139 0.62357239
 0.57879516 0.52988354 0.48170703 0.43645277]
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

![](img/2d2d3709e2cda26cabb38364afef8a6d.png)

**代码#4:变化的位置参数**

```
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 5, 100)

# Varying positional arguments
y1 = gilbrat.pdf(x, 1, 3)
y2 = gilbrat.pdf(x, 1, 4)
plt.plot(x, y1, "*", x, y2, "r--")
```

**输出:**
![](img/70519de604008d4846feae6f0ac3f15c.png)
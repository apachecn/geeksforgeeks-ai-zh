# scipy stats . gubel _ r()| python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/scipy-stats-gubel _ r-python/

**scipy.stats.gumbel_r()** 是一个右偏 gumbel 连续随机变量，用标准格式和一些形状参数来定义，以完成其规范。

![](img/451924f8db4579839e07a2a99eb0d8a8.png)

> **参数:**
> **- > q :** 上下尾概率
> **- > x :** 分位数
> **- > loc :** 【可选】位置参数。默认= 0
> **- >刻度:**【可选】刻度参数。默认值= 1
> **- >大小:**【整数元组，可选】形状或随机变量。
> **- >瞬间:**【可选】由字母['mvsk']组成；m’=均值，‘v’=方差，‘s’= Fisher 偏斜度，‘k’= Fisher 峰度。(默认值= 'mv ')。
> 
> **结果:**右偏 Gumbel 连续随机变量

**代码#1:创建右偏甘贝尔连续随机变量**

```
from scipy.stats import gumbel_r  

numargs = gumbel_r  .numargs
[] = [0.7, ] * numargs
rv = gumbel_r ()

print ("RV : \n", rv) 
```

**输出:**

```
RV : 
 <scipy.stats._distn_infrastructure.rv_frozen object at 0x000001E39A4600F0>

```

**代码#2:右偏甘贝尔随机变量和概率分布**

```
import numpy as np
quantile = np.arange (0.01, 1, 0.1)

# Random Variates
R = gumbel_r .rvs(scale = 2,  size = 10)
print ("Random Variates : \n", R)

# PDF
R = gumbel_r .pdf(quantile, loc = 0, scale = 1)
print ("\nProbability Distribution : \n", R)
```

**输出:**

```
Random Variates : 
 [ 0.55349097 -0.36709655 -0.25581806 -0.81730142  0.28719592 -0.30831366
 -2.69858598 -0.23586469 -1.01965346  6.44132721]

Probability Distribution : 
 [0.36786111 0.36573943 0.36038433 0.35223844 0.34175873 0.32939568
 0.31557754 0.3006994  0.28511631 0.26913983]
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

![](img/ef189ac8a56f54c94aa6130cb37fce32.png)

**代码#4:变化的位置参数**

```
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 5, 100)

# Varying positional arguments
y1 = gumbel_r .pdf(x, 1, 3)
y2 = gumbel_r .pdf(x, 1, 4)
plt.plot(x, y1, "*", x, y2, "r--")
```

**输出:**
![](img/7dda3ee0fc6fc3a88b65cdfc728c4d27.png)
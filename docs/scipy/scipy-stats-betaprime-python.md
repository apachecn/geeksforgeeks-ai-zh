# scipy stats . beta prime()| python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/scipy-stats-beta prime python/

**scipy.stats.betaprime()** 是一个 betaprime 连续随机变量，用标准格式和一些形状参数定义，以完成其规格。

![](img/8cbcd8b3927a898e7bb1d2ff03c9e8e0.png)

> **参数:**
> **q :** 上下尾概率
> **a、b :** 形状参数
> **x :** 分位数
> **loc :** 【可选】位置参数。默认= 0
> **比例:**【可选】比例参数。默认值= 1
> **大小:**【整数元组，可选】形状或随机变量。
> **矩:**【可选】由字母['mvsk']组成；m’=均值，‘v’=方差，‘s’= Fisher 偏斜度，‘k’= Fisher 峰度。(默认值= 'mv ')。
> 
> **结果:**β素连续随机变量

**代码#1:创建β素连续随机变量**

```py
# importing scipy
from scipy.stats import betaprime

numargs = betaprimeprime.numargs
[a, b] = [0.6, ] * numargs
rv = betaprimeprime(a, b)

print ("RV : \n", rv)
```

**输出:**

```py
RV : 
 <scipy.stats._distn_infrastructure.rv_frozen object at 0x0000029482FCC438>

```

**代码# 2:β素随机变量和概率分布。**

```py
import numpy as np
quantile = np.arange (0.01, 1, 0.1)

# Random Variates
R = betaprime.rvs(a, b, scale = 2,  size = 10)
print ("Random Variates : \n", R)

# PDF
R = betaprime.pdf(quantile, a, b, loc = 0, scale = 1)
print ("\nProbability Distribution : \n", R) 
```

**输出:**

```py
Random Variates : 
 [ 1.59603917  1.92408727  1.2120992   0.34064091  2.68681773 22.99956678
  1.45523032  2.93360219 23.93717261 18.04203815]

Probability Distribution : 
 [2.58128122 0.8832351  0.61488062 0.47835546 0.39160163 0.33053737
 0.28490363 0.24941484 0.22101038 0.1977718 ]

```

**代码#3:图形表示。**

```py
import numpy as np
import matplotlib.pyplot as plt

distribution = np.linspace(0, np.minimum(rv.dist.b, 5))
print("Distribution : \n", distribution)

plot = plt.plot(distribution, rv.pdf(distribution))
```

**输出:**

```py
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

![](img/1b984d4e1c88444b70d072e196d3bd09.png)

**代码#4:变化的位置参数**

```py
from scipy.stats import arcsine
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 1.0, 100)

# Varying positional arguments
y1 = betaprime.pdf(x, 2.75, 2.75)
y2 = betaprime.pdf(x, 3.25, 3.25)
plt.plot(x, y1, "*", x, y2, "r--")
```

**输出:**
![](img/00e9091f7e640dc61cb454e676b66b8f.png)
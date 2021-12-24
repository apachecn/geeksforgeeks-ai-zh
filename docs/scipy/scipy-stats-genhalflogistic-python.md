# scipy stats . gen half logistic()| Python

> 原文:[https://www . geesforgeks . org/scipy-stats-gen half logistic-python/](https://www.geeksforgeeks.org/scipy-stats-genhalflogistic-python/)

**scipy . stats . gen half logistic()**是一个广义的半 logistic 连续随机变量，用标准格式和一些形状参数来定义，以完成其规格。

![](img/5f36626909b340bdf7f35371ece248a9.png)

> **参数:**
> **- > q :** 上下尾概率
> **- > x :** 分位数
> **- > loc :** 【可选】位置参数。默认= 0
> **- >刻度:**【可选】刻度参数。默认值= 1
> **- >大小:**【整数元组，可选】形状或随机变量。
> **- > a、b :** 形状参数
> **- >矩:**【可选】由字母['mvsk']组成；m’=均值，‘v’=方差，‘s’= Fisher 偏斜度，‘k’= Fisher 峰度。(默认值= 'mv ')。
> 
> **结果:**广义半逻辑连续随机变量

**代码#1:创建广义半逻辑连续随机变量**

```py
from scipy.stats import genhalflogistic 

numargs = genhalflogistic .numargs
[a] = [0.7, ] * numargs
rv = genhalflogistic (a)

print ("RV : \n", rv) 
```

**输出:**

```py
RV : 
 <scipy.stats._distn_infrastructure.rv_frozen object at 0x000001E39A2B2470>

```

**代码#2:广义半逻辑随机变量和概率分布**

```py
import numpy as np
quantile = np.arange (0.01, 1, 0.1)

# Random Variates
R = genhalflogistic.rvs(a, scale = 2,  size = 10)
print ("Random Variates : \n", R)

# PDF
R = genhalflogistic.pdf(a, quantile, loc = 0, scale = 1)
print ("\nProbability Distribution : \n", R)
```

**输出:**

```py
Random Variates : 
 [0.24206874 0.66813269 0.75441313 1.05887305 1.8791025  0.64401048
 2.11419943 0.62545354 1.57690457 1.64762353]

Probability Distribution : 
 [0.44618142 0.47576242 0.50958299 0.54863742 0.59426198 0.64829814
 0.71336075 0.7933007  0.89405304 1.02531554]
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
 [0\.         0.02915452 0.05830904 0.08746356 0.11661808 0.14577259
 0.17492711 0.20408163 0.23323615 0.26239067 0.29154519 0.32069971
 0.34985423 0.37900875 0.40816327 0.43731778 0.4664723  0.49562682
 0.52478134 0.55393586 0.58309038 0.6122449  0.64139942 0.67055394
 0.69970845 0.72886297 0.75801749 0.78717201 0.81632653 0.84548105
 0.87463557 0.90379009 0.93294461 0.96209913 0.99125364 1.02040816
 1.04956268 1.0787172  1.10787172 1.13702624 1.16618076 1.19533528
 1.2244898  1.25364431 1.28279883 1.31195335 1.34110787 1.37026239
 1.39941691 1.42857143]
```

![](img/ac21c889f7fb10dcc7cd39d988fcc98a.png)

**代码#4:变化的位置参数**

```py
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 5, 100)

# Varying positional arguments
y1 = genhalflogistic.pdf(x, a, 1, 3)
y2 = genhalflogistic.pdf(x, a, 1, 4)
plt.plot(x, y1, "*", x, y2, "r--")
```

**输出:**
![](img/04a23416a5c2f46c44be707afb9a6792.png)
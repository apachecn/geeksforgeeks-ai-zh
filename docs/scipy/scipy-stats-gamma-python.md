# scipy stats . gamma()| python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/scipy-stats-gamma-python/

**scipy.stats.gamma()** 是一个 gamma 连续随机变量，用标准格式和一些形状参数定义，以完成其规格。
T3】

> **参数:**
> **- > q :** 上下尾概率
> **- > x :** 分位数
> **- > loc :** 【可选】位置参数。默认= 0
> **- >刻度:**【可选】刻度参数。默认值= 1
> **- >大小:**【整数元组，可选】形状或随机变量。
> **- > a :** 形状参数
> **- >矩:**【可选】由字母['mvsk']组成；m’=均值，‘v’=方差，‘s’= Fisher 偏斜度，‘k’= Fisher 峰度。(默认值= 'mv ')。
> 
> **结果:**γ连续随机变量

**代码#1:创建伽玛连续随机变量**

```py
from scipy.stats import gamma 

numargs = gamma .numargs
[a] = [0.7, ] * numargs
rv = gamma (a)

print ("RV : \n", rv) 
```

**输出:**

```py
RV : 
 <scipy.stats._distn_infrastructure.rv_frozen object at 0x0000018D57997F60>

```

**代码#2:广义伽马随机变量。**

```py
import numpy as np
quantile = np.arange (0.01, 1, 0.1)

# Random Variates
R = gamma.rvs(a, scale = 2,  size = 10)
print ("Random Variates : \n", R)

# PDF
R = gamma.pdf(a, quantile, loc = 0, scale = 1)
print ("\nProbability Distribution : \n", R)
```

**输出:**

```py
Random Variates : 
 [0.01601209 0.05164555 1.22072489 0.53476245 0.11529018 0.16966403
 0.59198231 0.71995529 0.86063603 3.81492177]

Probability Distribution : 
 [0.00710916 0.07919869 0.15097014 0.21974949 0.28337498 0.34020629
 0.38910556 0.42939763 0.46081639 0.48344302]
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

![](img/e46e2084a0497154ce03299458f29533.png)

**代码#4:变化的位置参数**

```py
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 5, 100)

# Varying positional arguments
y1 = gamma.pdf(x, a, 1, 3)
y2 = gamma.pdf(x, a, 1, 4)
plt.plot(x, y1, "*", x, y2, "r--")
```

**输出:**
![](img/b3a01a884822f18c1a33d3da37712861.png)
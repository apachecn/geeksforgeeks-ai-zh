# scipy . stats . Expo()| python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/scipy-stats-expos-python/

**scipy.stats.expon()** 是一个指数连续随机变量，用标准格式和一些形状参数定义，以完成其规格。
T3】

> **参数:**
> **q :** 上下尾概率
> **x :** 分位数
> **loc :** 【可选】位置参数。默认= 0
> **比例:**【可选】比例参数。默认值= 1
> **大小:**【整数元组，可选】形状或随机变量。
> **瞬间:**【可选】由字母['mvsk']组成；m’=均值，‘v’=方差，‘s’= Fisher 偏斜度，‘k’= Fisher 峰度。(默认值= 'mv ')。
> 
> **结果:**指数连续随机变量

**代码#1:创建指数连续随机变量**

```py

from scipy.stats import expon 

numargs = expon.numargs
[ ] = [0.6, ] * numargs
rv = expon( )

print ("RV : \n", rv) 
```

**输出:**

```py
RV : 
 <scipy.stats._distn_infrastructure.rv_frozen object at 0x0000018D56531CC0>

```

**代码#2:指数随机变量和概率分布。**

```py
import numpy as np
quantile = np.arange (0.01, 1, 0.1)

# Random Variates
R = expon.rvs(scale = 2,  size = 10)
print ("Random Variates : \n", R)

# PDF
R = expon.pdf(quantile, loc = 0, scale = 1)
print ("\nProbability Distribution : \n", R)
```

**输出:**

```py
Random Variates : 
 [2.50259466e-04 4.32311862e+00 8.22833503e-01 1.63374263e+00
 4.46784023e+00 3.56781485e+00 3.95381396e+00 1.17623772e+00
 3.21834266e-02 4.14778445e+00]

Probability Distribution : 
 [0.99004983 0.89583414 0.81058425 0.73344696 0.66365025 0.60049558
 0.54335087 0.4916442  0.44485807 0.40252422]

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

![](img/d207e8fb4e1676f49f21b0a28521383b.png)

**代码#4:变化的位置参数**

```py
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 5, 100)

# Varying positional arguments
y1 = expon.pdf(x, 2, 6)
y2 = expon.pdf(x, 1, 4)
plt.plot(x, y1, "*", x, y2, "r--")
```

**输出:**
![](img/99565c9efdd3ba3439599611f5aaae2e.png)
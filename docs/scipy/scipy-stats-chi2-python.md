# scipy . stats . chi2()| Python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/scipy-stats-chi 2-python/

**scipy.stats.chi2()** 是一个卡方连续随机变量，用标准格式和一些形状参数定义，以完成其规格。

![](img/e3e49ae84ac2597d82e79ef64672a902.png)

> **参数:**
> **q :** 上下尾概率
> **x :** 分位数
> **loc :** 【可选】位置参数。默认= 0
> **比例:**【可选】比例参数。默认值= 1
> **大小:**【整数元组，可选】形状或随机变量。
> **瞬间:**【可选】由字母['mvsk']组成；m’=均值，‘v’=方差，‘s’= Fisher 偏斜度，‘k’= Fisher 峰度。(默认值= 'mv ')。
> 
> **结果:**卡方连续随机变量

**代码#1:创建卡方连续随机变量**

```
# importing scipy
from scipy.stats import chi2

numargs = chi2.numargs
[a] = [0.6, ] * numargs
rv = chi2(a)

print ("RV : \n", rv) 
```

**输出:**

```
RV : 
 <scipy.stats._distn_infrastructure.rv_frozen object at 0x0000029485196DD8>

```

**代码#2 : chi2 随机变量和概率分布函数。**

```
import numpy as np
quantile = np.arange (0.01, 1, 0.1)

# Random Variates
R = chi2.rvs(a, scale = 2,  size = 10)
print ("Random Variates : \n", R)

# PDF
R = chi2.pdf(a, quantile, loc = 0, scale = 1)
print ("\nProbability Distribution : \n", R)
```

**输出:**

```
Random Variates : 
 [6.20115012e-01 4.82717678e-01 1.43760444e-02 1.19755537e+00
 3.00093606e-05 6.11268950e-01 5.99940774e-01 3.20509994e-01
 1.94220599e-01 6.63225404e-01]

Probability Distribution : 
 [0.00615404 0.06544849 0.12034254 0.1704933  0.21568622 0.25581903
 0.29088625 0.32096438 0.34619796 0.36678666]

```

**代码#3:图形表示。**

```
import numpy as np
import matplotlib.pyplot as plt

distribution = np.linspace(0, np.minimum(rv.dist.b, 5))
print("Distribution : \n", distribution)

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

![](img/ca743c8b307049a3549aae735ff30a6b.png)

**代码#4:变化的位置参数**

```
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 5, 100)

# Varying positional arguments
y1 = chi2.pdf(x, 1, 6)
y2 = chi2.pdf(x, 1, 4)
plt.plot(x, y1, "*", x, y2, "r--")
```

**输出:**
![](img/2a438ef0a8c9744ccc8c1f04bb62a769.png)
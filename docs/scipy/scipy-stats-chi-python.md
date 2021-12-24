# scipy stats.chi() | Python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/scipy-stats-chi-python/

**scipy.stats.chi()** 是一个 chi 连续随机变量，用标准格式和一些形状参数定义，以完成其规格。

![](img/7d9abd20bfd77203b7a8e1fde0fa01ab.png)

> **参数:**
> **q :** 上下尾概率
> **x :** 分位数
> **loc :** 【可选】位置参数。默认= 0
> **比例:**【可选】比例参数。默认值= 1
> **大小:**【整数元组，可选】形状或随机变量。
> **瞬间:**【可选】由字母['mvsk']组成；m’=均值，‘v’=方差，‘s’= Fisher 偏斜度，‘k’= Fisher 峰度。(默认值= 'mv ')。
> 
> **结果:** chi 连续随机变量

**特殊情况:**

*   chi(1，loc，scale) = **半正常**
*   chi(2，0，刻度)= **瑞利**
*   chi(3，0，刻度):**麦克斯韦**

**代码#1:创建 chi 连续随机变量**

```
# importing scipy
from scipy.stats import chi 

numargs = chi.numargs
[a] = [0.6, ] * numargs
rv = chi(a)

print ("RV : \n", rv) 
```

**输出:**

```
RV : 
 <scipy.stats._distn_infrastructure.rv_frozen object at 0x000002948537C6D8>

```

**代码#2 : chi 随机变量和概率分布。**

```
import numpy as np
quantile = np.arange (0.01, 1, 0.1)

# Random Variates
R = chi.rvs(a, scale = 2,  size = 10)
print ("Random Variates : \n", R)

# PDF
R = chi.pdf(a, quantile, loc = 0, scale = 1)
print ("\nProbability Distribution : \n", R)
```

**输出:**

```
Random Variates : 
 [2.40483665 1.68478304 0.01664071 2.48977805 3.66286843 1.68463842
 0.14434643 0.67812242 0.46190886 1.99973997]

Probability Distribution : 
 [0.01384193 0.14349716 0.25719966 0.35519439 0.43801475 0.50641521
 0.56131243 0.60373433 0.63477687 0.65556791]

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

![](img/28f7b2799ffdd27453f95ecebc3d418c.png)

**代码#4:变化的位置参数**

```
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 5, 100)

# Varying positional arguments
y1 = chi.pdf(x, 1, 6)
y2 = chi.pdf(x, 1, 4)
plt.plot(x, y1, "*", x, y2, "r--")
```

**输出:**
![](img/2275eece84be56f48629c8555ca8ab1d.png)
# scipy stat . dgam()\ python

> 原文:[https://www.geeksforgeeks.org/scipy-stats-dgamma-python/](https://www.geeksforgeeks.org/scipy-stats-dgamma-python/)

**scipy.stats.dgamma ()** 是一个双伽玛连续随机变量，用标准格式和一些形状参数定义，以完成其规格。
T3】

> **参数:**
> **q :** 上下尾概率
> **x :** 分位数
> **loc :** 【可选】位置参数。默认= 0
> **比例:**【可选】比例参数。默认值= 1
> **大小:**【整数元组，可选】形状或随机变量。
> **瞬间:**【可选】由字母['mvsk']组成；m’=均值，‘v’=方差，‘s’= Fisher 偏斜度，‘k’= Fisher 峰度。(默认值= 'mv ')。
> 
> **结果:**双γ连续随机变量

**代码#1:创建双伽玛连续随机变量**

```
from scipy.stats import chi 

numargs = chi.numargs
[a] = [0.6, ] * numargs
rv = chi(a)

print ("RV : \n", rv) 
```

**输出:**

```
RV : 
 <scipy.stats._distn_infrastructure.rv_frozen object at 0x000001FDC8AA3940>

```

**代码#2:双伽玛随机变量和概率分布。**

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
 [-1.95099046 -0.92462647 -0.44728222 -1.02853811  0.26525202  0.33532233
 -1.74580986 -0.02263675  0.02631306  0.01852519]

Probability Distribution : 
 [0.00457609 0.05019958 0.09422768 0.13505809 0.1714982  0.20274293
 0.22833692 0.24812679 0.2622088  0.27087564]

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

![](img/827750b8c7a6dfcb8537e2fc2d4cc939.png)

**代码#4:变化的位置参数**

```
<div class="noIdeBtnDiv">
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 5, 100)

# Varying positional arguments
y1 = chi.pdf(x, 1, 6)
y2 = chi.pdf(x, 1, 4)
plt.plot(x, y1, "*", x, y2, "r--")
```
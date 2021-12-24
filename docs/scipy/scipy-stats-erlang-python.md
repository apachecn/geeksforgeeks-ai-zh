# scipy stats . Erlang()| Python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/scipy-stats-杨二郎-python/

**scipy.stats.erlang() :** 是一个 erlang 连续随机变量，用标准格式和一些形状参数定义，以完成其规范。这是伽玛分布的一个特例。

> **参数:**
> **q :** 上下尾概率
> **x :** 分位数
> **loc :** 【可选】位置参数。默认= 0
> **比例:**【可选】比例参数。默认值= 1
> **大小:**【整数元组，可选】形状或随机变量。
> **瞬间:**【可选】由字母['mvsk']组成；m’=均值，‘v’=方差，‘s’= Fisher 偏斜度，‘k’= Fisher 峰度。(默认值= 'mv ')。
> 
> **结果:**二郎连续随机变量

**代码#1:创建二郎连续随机变量**

```py
from scipy.stats import erlang 

numargs = erlang.numargs
[a] = [0.6, ] * numargs
rv = erlang(a)

print ("RV : \n", rv) 
```

**输出:**

```py
RV : 
 <scipy.stats._distn_infrastructure.rv_frozen object at 0x0000018D544FBC88>

```

**代码#2 : erlang 随机变量和概率分布。**

```py
import numpy as np
quantile = np.arange (0.01, 1, 0.1)

# Random Variates
R = erlang.rvs(a, scale = 2,  size = 10)
print ("Random Variates : \n", R)

# PDF
R = erlang.pdf(a, quantile, loc = 0, scale = 1)
print ("\nProbability Distribution : \n", R)
```

**输出:**

```py
Random Variates : 
 [5.65708510e+00 5.16045580e+00 1.02056956e-01 3.64349340e-01
 5.65593073e+00 2.27100280e+00 9.77623414e-04 2.01994399e-01
 8.84331471e-01 2.20817630e+00]

Probability Distribution :
[0.01, 0.11, 0.21, 0.31, 0.41, 0.51, 0.61, 0.71, 0.81, 0.91]

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

![](img/5eaa385ef28dc1a25d440ef8b94b1c53.png)

**代码#4:变化的位置参数**

```py
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 5, 100)

# Varying positional arguments
y1 = erlang.pdf(x, 2, 6)
y2 = erlang.pdf(x, 1, 4)
plt.plot(x, y1, "*", x, y2, "r--")
```

**输出:**
![](img/74e8f23618c00411e2eced8f6a92dde9.png)
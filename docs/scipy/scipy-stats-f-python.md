# scipy stats.f() | Python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/scipy-stats-f-python/

**scipy.stats.f()** 是一个 F 连续随机变量，用标准格式和一些形状参数来定义，以完成其规格。
T3】

> **参数:**
> **q :** 上下尾概率
> **a、b :** 形状参数
> **x :** 分位数
> **loc :** 【可选】位置参数。默认= 0
> **比例:**【可选】比例参数。默认值= 1
> **大小:**【整数元组，可选】形状或随机变量。
> **矩:**【可选】由字母['mvsk']组成；m’=均值，‘v’=方差，‘s’= Fisher 偏斜度，‘k’= Fisher 峰度。(默认值= 'mv ')。
> 
> **结果:** F 连续随机变量

**代码#1:创建 F 连续随机变量**

```py
from scipy.stats import f   

numargs = f.numargs
[a, b] = [0.6, ] * numargs
rv = f(a, b)

print ("RV : \n", rv) 
```

**输出:**

```py
RV : 
 <scipy.stats._distn_infrastructure.rv_frozen object at 0x0000018D566864A8>

```

**代码#2:指数 F 随机变量和概率分布。**

```py
import numpy as np
quantile = np.arange (0.01, 1, 0.1)

# Random Variates
R = f.rvs(a, b, scale = 2,  size = 10)
print ("Random Variates : \n", R)

# PDF
R = f.pdf(a, b, quantile, loc = 0, scale = 1)
print ("\nProbability Distribution : \n", R)
```

**输出:**

```py
Random Variates : 
 [2.77609532e+00 2.55454726e-04 7.77303742e+01 2.61642158e+02
 3.39772973e-01 8.63437666e+02 3.24316832e+02 5.88915362e+06
 1.27105242e+03 7.30691909e-01]

Probability Distribution : 
 [0.00800042 0.06746857 0.10587056 0.13291306 0.15295841 0.16837285
 0.18056559 0.19043041 0.19856155 0.2053691 ]

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

![](img/5f63fd345efb4e37a9bf38f58a725154.png)

**代码#4:变化的位置参数**

```py
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 5, 100)

# Varying positional arguments
y1 = f  .pdf(x, 2, 6)
y2 = f  .pdf(x, 1, 4)
plt.plot(x, y1, "*", x, y2, "r--")
```

**输出:**

![](img/40b1c8f5fe6dfbe3ee2fccd8c43c80a1.png)
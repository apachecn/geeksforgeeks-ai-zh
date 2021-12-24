# scipy stats . expondelle()| python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/scipy-stats-exposed women-python/

**scipy . stats . expoweib()**是一个指数威布尔连续随机变量，用标准格式和一些形状参数定义，以完成其规格。
T3】

> **参数:**
> **q :** 上下尾概率
> **x :** 分位数
> **loc :** 【可选】位置参数。默认= 0
> **比例:**【可选】比例参数。默认值= 1
> **大小:**【整数元组，可选】形状或随机变量。
> **瞬间:**【可选】由字母['mvsk']组成；m’=均值，‘v’=方差，‘s’= Fisher 偏斜度，‘k’= Fisher 峰度。(默认值= 'mv ')。
> 
> **结果:**指数威布尔连续随机变量

**代码#1:创建指数威布尔连续随机变量**

```
from scipy.stats import exponweib  

numargs = exponweib .numargs
[a, b] = [0.6, ] * numargs
rv = exponweib (a, b)

print ("RV : \n", rv) 
```

**输出:**

```
RV : 
 <scipy.stats._distn_infrastructure.rv_frozen object at 0x0000018D5660E1D0>

```

**代码#2:指数威布尔随机变量和概率分布。**

```
import numpy as np
quantile = np.arange (0.01, 1, 0.1)

# Random Variates
R = exponweib .rvs(a, b, scale = 2,  size = 10)
print ("Random Variates : \n", R)

# PDF
R = exponweib .pdf(a, b, quantile, loc = 0, scale = 1)
print ("\nProbability Distribution : \n", R)
```

**输出:**

```
Random Variates : 
 [8.17460511e+00 1.33286202e+00 1.77493153e+01 1.83861272e-01
 5.32255458e-01 1.34520149e+00 1.91022498e-02 3.08216056e-03
 6.46223522e-03 1.75786657e-01]

Probability Distribution : 
 [0.00442484 0.04919014 0.09470438 0.14070318 0.1869346  0.2331608
 0.27915913 0.32472306 0.36966267 0.41380492]

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

![](img/be2cc8387bcd722b5894b229c4dae0c7.png)

**代码#4:变化的位置参数**

```
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 5, 100)

# Varying positional arguments
y1 = exponweib .pdf(x, 2, 6)
y2 = exponweib .pdf(x, 1, 4)
plt.plot(x, y1, "*", x, y2, "r--")
```

**输出:**
![](img/8225fa44d6886f1b53db2c854250f7f9.png)
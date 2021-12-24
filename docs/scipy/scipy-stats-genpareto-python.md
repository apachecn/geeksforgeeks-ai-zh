# scipy stats . genpareto()| python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/scipy-stats-genpareto-python/

**scipy.stats.genpareto()** 是一个广义的 pareto 连续随机变量，用标准格式和一些形状参数来定义，以完成其规格。
T3】

> **参数:**
> **- > q :** 上下尾概率
> **- > a、b :** 形状参数
> **- > x :** 分位数
> **- > loc :** 【可选】位置参数。默认= 0
> **- >刻度:**【可选】刻度参数。默认值= 1
> **- >大小:**【整数元组，可选】形状或随机变量。
> **- >矩:**【可选】由字母['mvsk']组成；m’=均值，‘v’=方差，‘s’= Fisher 偏斜度，‘k’= Fisher 峰度。(默认值= 'mv ')。
> 
> **结果:**广义帕累托连续随机变量

**代码#1:创建广义帕累托连续随机变量**

```
from scipy.stats import genpareto 

numargs = genpareto .numargs
[a] = [0.7, ] * numargs
rv = genpareto (a)

print ("RV : \n", rv) 
```

**输出:**

```
RV : 
 <scipy.stats._distn_infrastructure.rv_frozen object at 0x0000018D579B85C0>

```

**代码#2:广义帕累托随机变量。**

```
import numpy as np
quantile = np.arange (0.01, 1, 0.1)

# Random Variates
R = genpareto.rvs(a, scale = 2,  size = 10)
print ("Random Variates : \n", R)
```

**输出:**

```
Random Variates : 
 [ 1.55978773  0.03897083  7.68148511  0.78339525  1.1217962   0.20434352
  1.16663003  2.06115353 12.82886098  0.27780119]
```

**代码#3:图形表示。**

```
import numpy as np
import matplotlib.pyplot as plt

distribution = np.linspace(0, np.minimum(rv.dist.b, 3))
print("Distribution : \n", distribution)

plot = plt.plot(distribution, rv.pdf(distribution))
```

**输出:**

```
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

![](img/43000b11047a3971841f018598192d51.png)

**代码#4:变化的位置参数**

```
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 5, 100)

# Varying positional arguments
y1 = genpareto.pdf(x, 1, 3)
y2 = genpareto.pdf(x, 1, 4)
plt.plot(x, y1, "*", x, y2, "r--")
```

**输出:**
![](img/4bb1a0e9203c2e0d0c12156e67edef7e.png)
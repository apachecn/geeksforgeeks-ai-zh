# scipy stats . genexpon()| python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/scipy-stats-genexpon-python/

**scipy.stats.genexpon()** 是一个广义指数连续随机变量，用标准格式和一些形状参数来定义，以完成其规格。

> **参数:**
> **- > q :** 上下尾概率
> **- > x :** 分位数
> **- > loc :** 【可选】位置参数。默认= 0
> **- >刻度:**【可选】刻度参数。默认值= 1
> **- >大小:**【整数元组，可选】形状或随机变量。
> **- > a、b、c :** 形状参数
> **- >矩:**【可选】由字母['mvsk']组成；m’=均值，‘v’=方差，‘s’= Fisher 偏斜度，‘k’= Fisher 峰度。(默认值= 'mv ')。
> 
> **结果:**广义指数连续随机变量

**代码#1:创建广义指数连续随机变量**

```py
from scipy.stats import genexpon 

numargs = genexpon .numargs
[a, b, c] = [0.7, ] * numargs
rv = genexpon (a, b, c)

print ("RV : \n", rv) 
```

**输出:**

```py
RV : 
 <scipy.stats._distn_infrastructure.rv_frozen object at 0x0000018D57997F60>

```

**代码#2:广义指数随机变量。**

```py
import numpy as np
quantile = np.arange (0.01, 1, 0.1)

# Random Variates
R = genexpon.rvs(a, scale = 2,  size = 10)
print ("Random Variates : \n", R)
```

**输出:**

```py
Random Variates : 
 [0.74505484 2.02790441 2.06823675 3.96275674 1.24274054 3.71331036
 0.53957521 0.37359838 2.53934153 2.36254065]

Probability Distribution : 
 [0.43109163 0.45222638 0.47102054 0.48773188 0.50258763 0.51578837
 0.52751153 0.53791424 0.54713591 0.55530037]
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

![](img/680059c45501d7333498d0438e3d91de.png)

**代码#4:变化的位置参数**

```py
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 5, 100)

# Varying positional arguments
y1 = genexpon.pdf(x, a, 1, 3)
y2 = genexpon.pdf(x, a, 1, 4)
plt.plot(x, y1, "*", x, y2, "r--")
```

**输出:**
![](img/468dcb8cbcf4abf6ca59b0d4c4a81161.png)
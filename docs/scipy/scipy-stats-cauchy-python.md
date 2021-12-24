# scipy stats . Cauchy()| Python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/scipy-stats-Cauchy-python/

**scipy.stats.cauchy()** 是一个 cauchy 连续随机变量，用标准格式和一些形状参数定义，以完成其规格。

![](img/47fce215ebbd2b0226f8703e1a7ebe6f.png)

> **参数:**
> **q :** 上下尾概率
> **x :** 分位数
> **loc :** 【可选】位置参数。默认= 0
> **比例:**【可选】比例参数。默认值= 1
> **大小:**【整数元组，可选】形状或随机变量。
> **瞬间:**【可选】由字母['mvsk']组成；m’=均值，‘v’=方差，‘s’= Fisher 偏斜度，‘k’= Fisher 峰度。(默认值= 'mv ')。
> 
> **结果:**柯西连续随机变量

**代码#1:创建柯西连续随机变量**

```py
# importing scipy
from scipy.stats import cauchy

numargs = cauchy.numargs
[] = [0.6, ] * numargs
rv = cauchy()

print ("RV : \n", rv) 
```

**输出:**

```py
RV : 
 <scipy.stats._distn_infrastructure.rv_frozen object at 0x000002948548C6D8>

```

**代码#2:柯西随机变量和概率分布函数。**

```py
import numpy as np
quantile = np.arange (0.01, 1, 0.1)

import numpy as np
import matplotlib.pyplot as plt

distribution = np.linspace(0, np.minimum(rv.dist.b, 5))
print("Distribution : \n", distribution)

plot = plt.plot(distribution, rv.pdf(distribution))
```

**输出:**

```py
Random Variates : 
 [ 2.73388202  4.88389383 -4.89271415  4.63864536 -0.36933865  1.51521875
  1.43853452 -0.69619917 -0.68358229  4.13179831]

Probability Distribution : 
 [0.31827806 0.31450438 0.30486533 0.29040223 0.27250226 0.25260685
 0.23198738 0.21162814 0.19220451 0.17412061]
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

![](img/7ba2875265e3e8efa3aa2935fe51bf8a.png)

**代码#4:变化的位置参数**

```py
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 1.0, 100)

# Varying positional arguments
y1 = cauchy.pdf(x, 2.75, 2.75)
y2 = cauchy.pdf(x, 3.25, 3.25)
plt.plot(x, y1, "*", x, y2, "r--")
```

**输出:**
![](img/a894dff7809b5ddecd857b5b4b2f1ad3.png)
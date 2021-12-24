# scipy stats . genextreme()| python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/scipy-stats-genextreme-python/

**scipy . stats . genetxtreme()**是一个广义极值连续随机变量，用标准格式和一些形状参数来定义，以完成其规范。

> **参数:**
> **- > q :** 上下尾概率
> **- > x :** 分位数
> **- > loc :** 【可选】位置参数。默认= 0
> **- >刻度:**【可选】刻度参数。默认值= 1
> **- >大小:**【整数元组，可选】形状或随机变量。
> **- > a、b、c :** 形状参数
> **- >矩:**【可选】由字母['mvsk']组成；m' =均值，' v' =方差，
> 's' =费雪偏斜度，' k' =费雪峰度。(默认值= 'mv ')。
> 
> **结果:**广义极值连续随机变量

**为 a==0**
![](img/cb582ce139ae91da54471720e3ed04ca.png)

**为 x < = 1/a，a>0**
T3】

**代码#1:创建广义极值连续随机变量**

```
from scipy.stats import genextreme 

numargs = genextreme .numargs
[a] = [0.7, ] * numargs
rv = genextreme (a)

print ("RV : \n", rv) 
```

**输出:**

```
RV : 
 <scipy.stats._distn_infrastructure.rv_frozen object at 0x000001E399AB5A58>

```

**代码#2:广义极值随机变量。**

```
import numpy as np
quantile = np.arange (0.01, 1, 0.1)

# Random Variates
R = genextreme.rvs(a, scale = 2,  size = 10)
print ("Random Variates : \n", R)

# PDF
R = genextreme.pdf(a, quantile, loc = 0, scale = 1)
print ("\nProbability Distribution : \n", R)
```

**输出:**

```
Random Variates : 
 [ 1.0976659  -4.30499477 -1.30818332  1.54664658  1.44268486  1.80027137
  1.52868675  1.8569798   1.36066713 -1.85945751]

Probability Distribution : 
 [0.30397758 0.32272193 0.34399063 0.3683456  0.39653387 0.42957283
 0.46888883 0.51655345 0.57571147 0.65141728]
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
 [0\.         0.02915452 0.05830904 0.08746356 0.11661808 0.14577259
 0.17492711 0.20408163 0.23323615 0.26239067 0.29154519 0.32069971
 0.34985423 0.37900875 0.40816327 0.43731778 0.4664723  0.49562682
 0.52478134 0.55393586 0.58309038 0.6122449  0.64139942 0.67055394
 0.69970845 0.72886297 0.75801749 0.78717201 0.81632653 0.84548105
 0.87463557 0.90379009 0.93294461 0.96209913 0.99125364 1.02040816
 1.04956268 1.0787172  1.10787172 1.13702624 1.16618076 1.19533528
 1.2244898  1.25364431 1.28279883 1.31195335 1.34110787 1.37026239
 1.39941691 1.42857143]
```

![](img/e2043f3256b124d7a9b9f5c3b217bc59.png)

**代码#4:变化的位置参数**

```
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 5, 100)

# Varying positional arguments
y1 = genextreme.pdf(x, a, 1, 3)
y2 = genextreme.pdf(x, a, 1, 4)
plt.plot(x, y1, "*", x, y2, "r--")
```

**输出:**
![](img/079d9aaa8ac66a558eb3db8c214f3df1.png)
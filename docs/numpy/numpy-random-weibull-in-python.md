# Python 中的 numpy.random.weibull()

> 原文:[https://www . geesforgeks . org/numpy-random-Weibull-in-python/](https://www.geeksforgeeks.org/numpy-random-weibull-in-python/)

借助 **numpy.random.weibull()** 方法，我们可以从 weibull 分布中获取随机样本，并利用该方法将随机样本作为 numpy 数组返回。

![](img/47cc46bc94d676c1736eb8b9fe23f3ba.png)

威布尔分布

> **语法:** numpy.random.weibull(a，size=None)
> 
> **返回:**将随机样本作为 numpy 数组返回。

**示例#1 :**

在这个例子中我们可以看到，通过使用 **numpy.random.weibull()** 方法，我们能够从 weibull 分布中获得随机样本并返回 numpy 数组。

## 蟒蛇 3

```
# import numpy
import numpy as np
import matplotlib.pyplot as plt

# Using weibull() method
gfg = np.random.weibull(5, 5000)

plt.hist(gfg, bins = 50, density = True)
plt.show()
```

**输出:**

> ![](img/3de48ccdda066142fe9ff008b713e9c5.png)

**例 2 :**

## 蟒蛇 3

```
# import numpy
import numpy as np
import matplotlib.pyplot as plt

# Using weibull() method
gfg = np.random.weibull(6.78, 10000)

plt.hist(gfg, bins = 100, density = True)
plt.show()
```

**输出:**

> ![](img/c0391579581691fde34f3973f7a12533.png)
# Python 中的 numpy.random.uniform()

> 原文:[https://www . geesforgeks . org/numpy-random-uniform-in-python/](https://www.geeksforgeeks.org/numpy-random-uniform-in-python/)

借助 **numpy.random.uniform()** 方法，我们可以从均匀分布中得到随机样本，并利用该方法将随机样本作为 numpy 数组返回。

![](img/42b291f6c10e9b30732d21e2d81a518c.png)

均匀分布

> **语法:** numpy.random.uniform(低=0.0，高=1.0，大小=无)
> 
> **返回:**将随机样本作为 numpy 数组返回。

**示例#1 :**

在这个例子中我们可以看到，通过使用 **numpy.random.uniform()** 方法，我们能够从均匀分布中获得随机样本并返回随机样本。

## 蟒蛇 3

```
# import numpy
import numpy as np
import matplotlib.pyplot as plt

# Using uniform() method
gfg = np.random.uniform(-5, 5, 5000)

plt.hist(gfg, bins = 50, density = True)
plt.show()
```

**输出:**

> ![](img/a127ed5035e9f42f2e3a4c3b0964bb7a.png)

**例 2 :**

## 蟒蛇 3

```
# import numpy
import numpy as np
import matplotlib.pyplot as plt

# Using uniform() method
gfg = np.random.uniform(2.1, 5.5, 10000)

plt.hist(gfg, bins = 100, density = True)
plt.show()
```

**输出:**

> ![](img/336f3b9b97c419b83b1066d09f6f2783.png)
# Python 中的 numpy.random.zipf()

> 原文:[https://www.geeksforgeeks.org/numpy-random-zipf-in-python/](https://www.geeksforgeeks.org/numpy-random-zipf-in-python/)

借助于 **numpy.random.zipf()** 方法，我们可以从 zipf 分布中获取随机样本，并利用该方法将随机样本作为 numpy 数组返回。

![](img/5fdd0c0e685bbaba515279f9ea722677.png)

Zipf 分布

> **语法:** numpy.random.zipf(a，size=None)
> 
> **返回:**将随机样本作为 numpy 数组返回。

**示例#1 :**

在这个例子中我们可以看到，通过使用 **numpy.random.zipf()** 方法，我们能够从 zipf 分布中获得随机样本，并将随机样本作为 numpy 数组返回。

## 蟒蛇 3

```
# import numpy
import numpy as np
import matplotlib.pyplot as plt

# Using zipf() method
gfg = np.random.zipf(2.7, 5000)

plt.hist(gfg, bins = 50, density = True)
plt.show()
```

**输出:**

> ![](img/2fa7689eb3c47cb1416b1e49ab4bf426.png)

**例 2 :**

## 蟒蛇 3

```
# import numpy
import numpy as np
import matplotlib.pyplot as plt

# Using zipf() method
gfg = np.random.zipf(4, 10000)

plt.hist(gfg, bins = 50, density = True)
plt.show()
```

**输出:**

> ![](img/95f5685d64497a494356dcce2d73dccb.png)
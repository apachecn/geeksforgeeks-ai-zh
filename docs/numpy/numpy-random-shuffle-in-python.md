# python 中的 numpy.random.shuffle()

> 原文:[https://www . geesforgeks . org/numpy-random-shuffle-in-python/](https://www.geeksforgeeks.org/numpy-random-shuffle-in-python/)

借助 **numpy.random.shuffle()** 方法，我们可以得到不同整数值在 numpy 数组中的随机定位，也可以说一个数组中的所有数值都会被随机洗牌。

> **语法:** numpy.random.shuffle(x)
> 
> **返回:**返回洗牌后的 numpy 数组。

**示例#1 :**

在这个例子中，我们可以看到通过使用 **numpy.random.shuffle()** 方法，我们能够对 numpy 数组中的值进行重新缓冲，或者改变数组中值的位置。

## 蟒蛇 3

```
# import numpy
import numpy as np
import matplotlib.pyplot as plt

gfg = np.arange(10)
# Using shuffle() method
np.random.shuffle(gfg)

print(gfg)
```

**输出:**

> [7 1 5 0 8 4 3 9 6 2]

**例 2 :**

## 蟒蛇 3

```
# import numpy
import numpy as np
import matplotlib.pyplot as plt

gfg = np.arange(16).reshape((4, 4))
# Using shuffle() method
np.random.shuffle(gfg)

print(gfg)
```

**输出:**

> [[ 4  5  6  7]
> 
> [ 0  1  2  3]
> 
> [ 8  9 10 11]
> 
> [12 13 14 15]]
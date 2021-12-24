# 使用 NumPy

从正态分布生成五个随机数

> 原文:[https://www . geeksforgeeks . org/从正态分布生成五个随机数-使用-numpy/](https://www.geeksforgeeks.org/generate-five-random-numbers-from-the-normal-distribution-using-numpy/)

在 Numpy 中，我们被提供了一个称为随机模块的模块，它允许我们使用随机数。随机模块提供了不同的数据分发方法。在本文中，我们必须创建一个指定形状的数组，并填充随机数或值，使这些值成为正态分布或高斯分布的一部分。这种分布也被称为钟形曲线，这是因为它的形状特征。

为了从正态分布生成五个随机数，我们将使用随机模块的 numpy.random.normal()方法。

> **语法:** numpy.random.normal(loc = 0.0，scale = 1.0，size = None)
> 
> **参数:**
> 
> **loc:** 分布平均值
> 
> **标度:**标准偏差
> 
> **尺寸:**合成形状。
> 如果 size 参数为空，则默认情况下返回单个值。

**例 1:**

## 蟒蛇 3

```
# importing module
import numpy as np

# numpy.random.normal() method
r = np.random.normal(size=5)

# printing numbers
print(r)
```

**输出:**

```
[ 0.27491897 -0.18001994 -0.01783066  1.07701319 -0.11356911]

```

**例 2:**

## 蟒蛇 3

```
# importing module
import numpy as np

# numpy.random.normal() method
random_array = np.random.normal(0.0, 1.0, 5)

# printing 1D array with random numbers
print("1D Array with random values : \n", random_array)
```

**输出:**

```
1D Array with random values :
[ 0.14559212  1.97263406  1.11170937 -0.88192442  0.8249291 ]

```
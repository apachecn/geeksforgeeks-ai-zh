# 设置 matplotlib

中的彩色范围

> 原文:[https://www . geesforgeks . org/set-color bar-range-in-matplotlib/](https://www.geeksforgeeks.org/set-colorbar-range-in-matplotlib/)

你好极客们！在本文中，我们将尝试使用 matplotlib Python 模块设置颜色范围。Matplotlib 允许我们进行大范围的 Colorbar 定制。颜色条只是 plt.Axes 的一个实例。它根据图表中的数据为数字与颜色的比率提供了一个标度。设置范围将颜色限制在一个子部分，颜色条错误地传达了数据下限与其上限相当的信息。通过这两种不同的限制，您可以控制颜色条的范围和图例。

**要求:** Matplotlib，NumPy

用于安装 Matplotlib

```py
pip install matplotlib
```

用于安装 Numpy。

```py
pip install numpy
```

**让我们通过分步实现来理解:**

**第一步:**

导入所需的库并设置一些通用数据。

## 蟒蛇 3

```py
import numpy as np
import matplotlib.pyplot as plt

# setup some generic data
N = 37
x, y = np.mgrid[:N, :N]
Z = (np.cos(x*0.2) + np.sin(y*0.3))
```

**第二步:**

屏蔽掉负值和正值。

## 蟒蛇 3

```py
Zpos = np.ma.masked_less(Z, 0)
Zneg = np.ma.masked_greater(Z, 0)
```
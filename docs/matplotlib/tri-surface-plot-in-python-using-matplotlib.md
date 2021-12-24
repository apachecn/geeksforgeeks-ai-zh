# 使用 Matplotlib 在 Python 中绘制三面图

> 原文:[https://www . geeksforgeeks . org/三面-python 中的绘图-使用-matplotlib/](https://www.geeksforgeeks.org/tri-surface-plot-in-python-using-matplotlib/)

一个**三面图**是一种曲面图，通过三角剖分有限个三角形的紧致曲面来创建，这些三角形以曲面上每个点都是三角形的方式覆盖整个曲面。任何两个三角形的交集都会导致空的或公共的边或顶点。这种类型的绘图是在均匀采样的网格限制和不方便绘图的地方创建的。一般通过调用 [matplotlib](https://www.geeksforgeeks.org/python-matplotlib-an-overview/) 库的 ax.plot_trisurf()函数来创建三曲面图。该功能的一些属性如下:

<figure class="table">

| 属性 | 参数 |
| --- | --- |
| X、Y、Z | 数据集作为 1D 数组进行绘制 |
| 颜色 | 表面斑块的颜色 |
| cmap | 颜色映射设置表面斑块的颜色 |
| norm | 参数对颜色的映射值进行归一化 |
| vmin |

</figure>

**示例 1:** 让我们使用 ax.plot_trisurf()函数创建一个基本的三曲面图。

## 蟒 3

```py
# Import libraries
from mpl_toolkits import mplot3d
import numpy as np
import matplotlib.pyplot as plt

# Creating dataset
z = np.linspace(0, 50000, 100)
x = np.sin(z)
y = np.cos(z)

# Creating figure
fig = plt.figure(figsize =(14, 9))
ax = plt.axes(projection ='3d')

# Creating plot
ax.plot_trisurf(x, y, z,
                linewidth = 0.2,
                antialiased = True);

# show plot
plt.show()
```
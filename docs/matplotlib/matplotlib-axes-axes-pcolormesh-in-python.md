# matplotlib . axes . pconlormesh()用 Python

表示

> 哎哎哎:# t0]https://www . geeksforgeeks . org/matplotlib-axes-pcolormesh-in-python/

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**轴类**包含了大部分的图形元素:轴、刻度、线二维、文本、多边形等。，并设置坐标系。Axes 的实例通过回调属性支持回调。

## matplotlib . axes . axes . pconlormesh()函数

matplotlib 库的 Axes 模块中的 **Axes.pcolormesh()函数**也用于创建具有非规则矩形网格的伪彩色图。对于给定的目的，它比 pcolor 更专业，因此速度更快。它支持古罗阴影

> **语法:** Axes.pcolormesh(self，*args，alpha=None，norm=None，cmap=None，vmin=None，vmax=None，底纹='flat '，抗锯齿=False，数据=None，**kwargs)
> 
> **参数:**该方法接受以下描述的参数:
> 
> *   **C :** 此参数包含 2D 阵列中要进行颜色映射的值。
> *   **X，Y:** 这些参数是四边形角的坐标。
> *   **cmap :** 此参数是一个 colormap 实例或注册的 colormap 名称。
> *   **norm :** 此参数是 Normalize 实例，它将数据值缩放到标准颜色映射范围[0，1]，以映射到颜色
> *   **vmin，vmax :** 这些参数本质上是可选，它们是 colorbar 范围。
> *   **alpha :** 此参数是颜色的强度。
> *   **捕捉:**此参数用于将网格捕捉到像素边界。
> *   **边缘颜色:**该参数是边缘的颜色。{ '无'，无，'脸'，颜色，颜色序列}
> *   **底纹:**此参数为填充样式。它可以是平的或高的。
> 
> **返回:**这将返回以下内容:
> 
> *   **网格:**这将返回**网格**

下面的例子说明了 matplotlib.axes . axes . pcolormesh()函数在 matplotlib . axes 中的作用:

**示例-1:**

```py
# Implementation of matplotlib function
import matplotlib.pyplot as plt
import numpy as np
from matplotlib.colors import LogNorm

Z = np.random.rand(25, 25)

fig, ax0 = plt.subplots()

ax0.pcolormesh(Z)

ax0.set_title('matplotlib.axes.Axes.pcolormesh() Examples')
plt.show()
```

**输出:**
![](img/2378c0296dc724b874acaafbf3f2e5be.png)

**示例-2:**

```py
# Implementation of matplotlib function
import matplotlib.pyplot as plt
import numpy as np
from matplotlib.colors import LogNorm

dx, dy = 0.015, 0.05
y, x = np.mgrid[slice(-4, 4 + dy, dy),
                slice(-4, 4 + dx, dx)]
z = (1 - x / 3\. + x ** 6 + y ** 3) * np.exp(-x ** 2 - y ** 2)
z = z[:-1, :-1]
z_min, z_max = -np.abs(z).max(), np.abs(z).max()

fig, ax = plt.subplots()

c = ax.pcolormesh(x, y, z, cmap ='Greens', vmin = z_min,
                  vmax = z_max)

fig.colorbar(c, ax = ax)
ax.set_title('matplotlib.axes.Axes.pcolormesh() Examples')
plt.show()
```

**输出:**
![](img/dbe08bbf0cbbb03335087837720493d6.png)
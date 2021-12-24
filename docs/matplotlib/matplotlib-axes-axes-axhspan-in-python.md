# matplotlib . axes . axhspan()在 Python

中

> 原文:[https://www . geeksforgeeks . org/matplotlib-axes-axes-axhs pan-in-python/](https://www.geeksforgeeks.org/matplotlib-axes-axes-axhspan-in-python/)

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**轴类**包含了大部分的图形元素:轴、刻度、线二维、文本、多边形等。，并设置坐标系。Axes 的实例通过回调属性支持回调。

## matplotlib.axes.Axes.axhspan()函数

matplotlib 库的 Axes 模块中的 **Axes.axhspan()函数**用于添加一个横跨轴的水平跨度(矩形)。

> **语法:**
> 
> ```
> Axes.axhspan(self, ymin, ymax, xmin=0, xmax=1, **kwargs)
> ```
> 
> **参数:**该方法接受以下描述的参数:
> 
> *   **ymin:** 该参数是以数据单位表示的水平跨度的下限。
> *   **ymax:** 此参数是以数据单位表示的水平跨度上限。
> *   **xmin:** 此参数是以数据单位表示的垂直跨度的下限。
> *   **xmax:** 此参数是以数据单位表示的垂直跨度上限。
> 
> **返回:**返回多边形。

下面的例子说明了 matplotlib.axes . axes pan()函数在 matplotlib . axes 中的作用:

**示例-1:**

```
# Implementation of matplotlib function
import matplotlib.pyplot as plt
import numpy as np

fig, ax = plt.subplots()

ax.axhspan(1.25, 1.55, facecolor ='g', alpha = 0.5)

ax.set_title('matplotlib.axes.Axes.axhspan() Example')

plt.show()
```

**输出:**
![](img/e3d64a85119cbdab3072a99d6c8e213b.png)

**示例-2:**

```
# Implementation of matplotlib function
import numpy as np
import matplotlib.pyplot as plt

t = np.arange(-2, 3, .01)
s = np.sin(np.pi * t)

fig, ax = plt.subplots()
ax.plot(t, s, color ='black')
ax.axhline(y = 1, color ='black')
ax.axvline(x = 1, color ='black')
ax.axvline(x = 0, ymin = 0.75, linewidth = 8, color ='green')
ax.axhline(y =.5, xmin = 0.25, xmax = 0.75, color ='black')

ax.axhspan(0.25, 0.75, facecolor ='0.5', alpha = 0.5)
ax.axvspan(1.25, 1.55, facecolor ='green', alpha = 0.5)

ax.set_title('matplotlib.axes.Axes.axhspan() Example')

plt.show()
```

**输出:**
![](img/cfd5434652b40655696a22073dac80f6.png)
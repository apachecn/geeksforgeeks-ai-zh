# Python 中的 matplotlib . axes . axes . get _ clip _ path()

> 原文:[https://www . geeksforgeeks . org/matplotlib-axes-axes-get _ clip _ path-in-python/](https://www.geeksforgeeks.org/matplotlib-axes-axes-get_clip_path-in-python/)

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**轴类**包含了大部分的图形元素:轴、刻度、线二维、文本、多边形等。，并设置坐标系。Axes 的实例通过回调属性支持回调。

## matplotlib . axes . axes . get _ clip _ path()函数

matplotlib 库的 Axes 模块中的 **Axes.get_clip_path()函数**用于获取裁剪路径。

> **语法:** Axes.get_clip_path(self)
> 
> **参数:**该方法不接受任何参数。
> 
> **返回:**此方法返回剪辑路径。

下面的例子说明了 matplotlib.axes . axes . get _ clip _ path()函数在 matplotlib . axes 中的作用:

**例 1:**

**输入图像:**

![geek-1](img/7ba6fa5912389e3b043bbcb25a460a5c.png)

```
# Implementation of matplotlib function
import matplotlib.pyplot as plt
import matplotlib.patches as patches
import matplotlib.cbook as cbook

with cbook.get_sample_data('geek.jpg') as image_file:
    image = plt.imread(image_file)

fig, ax = plt.subplots()
im = ax.imshow(image)

patch = patches.Rectangle((0, 0), 
                          260,
                          200, 
                          transform = ax.transData)

if im.get_clip_path() is None:
    im.set_clip_path(patch)

fig.suptitle('matplotlib.axes.Axes.get_clip_path() \
function Example\n\n', fontweight ="bold")

plt.show()
```

**输出:**
![](img/9691ad5abb6276f0cadf8cf3762a81dd.png)

**例 2:**

```
# Implementation of matplotlib function
import numpy as np
import matplotlib.cm as cm
import matplotlib.pyplot as plt
from matplotlib.path import Path
from matplotlib.patches import PathPatch

delta = 0.025

x = y = np.arange(-3.0, 3.0, delta)
X, Y = np.meshgrid(x, y)

Z1 = np.exp(-X**2 - Y**2)
Z2 = np.exp(-(X - 1)**2 - (Y - 1)**2)
Z = (Z1 - Z2) * 2

path = Path([[0, 1], [1, 0], [0, -1],
             [-1, 0], [0, 1]])

patch = PathPatch(path, facecolor ='none')

fig, ax = plt.subplots()
ax.add_patch(patch)

im = ax.imshow(Z, 
               interpolation ='bilinear', 
               cmap = cm.gray,
               origin ='lower',
               extent =[-3, 3, -3, 3],
               clip_path = patch,
               clip_on = True)

ax.text(-2.8, 2, str(im.get_clip_path()))

fig.suptitle('matplotlib.axes.Axes.get_clip_path() \
function Example\n\n', fontweight ="bold")

plt.show()
```

**输出:**
![](img/ab20d91dd629f404f808c588d9280fc1.png)
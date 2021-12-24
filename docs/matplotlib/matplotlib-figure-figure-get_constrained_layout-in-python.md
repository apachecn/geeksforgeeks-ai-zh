# Python 中的 matplotlib . figure . figure . get _ constrained _ layout()

> 原文:[https://www . geesforgeks . org/matplotlib-figure-figure-get _ constraint _ layout-in-python/](https://www.geeksforgeeks.org/matplotlib-figure-figure-get_constrained_layout-in-python/)

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**人物模块**提供了顶级的艺术家，人物，包含了所有的剧情元素。该模块用于控制所有情节元素的子情节和顶层容器的默认间距。

## matplotlib . figure . figure . get _ constraint _ layout()方法

**matplotlib 库的图形模块的 get_constrained_layout()方法**用于获取是否正在使用约束布局。

> **语法:** get_constrained_layout(自身)
> 
> **参数:**此方法不接受任何参数。
> 
> **返回:**该方法返回是否正在使用约束布局。

以下示例说明了 matplotlib.figure . figure . get _ constrained _ layout()函数在 matplotlib . figure 中的作用:

**例 1:**

```py
# Implementation of matplotlib function
import matplotlib.pyplot as plt
from matplotlib.lines import Line2D
import numpy as np
from numpy.random import rand

fig, ax2 = plt.subplots()

ax2.bar(range(10), rand(10), picker = True)
for label in ax2.get_xticklabels(): 
    label.set_picker(True)

def onpick1(event):

    if isinstance(event.artist, Line2D):
        thisline = event.artist

        xdata = thisline.get_xdata()
        ydata = thisline.get_ydata()

        ind = event.ind
        print('onpick1 line:',
               np.column_stack([xdata[ind],
                                ydata[ind]]))

    elif isinstance(event.artist, Rectangle):
        patch = event.artist
        print('onpick1 patch:', patch.get_path())

    elif isinstance(event.artist, Text):
        text = event.artist
        print('onpick1 text:', text.get_text())

print("Value return by get_constrained_layout() :", 
       fig.get_constrained_layout())

fig.suptitle('matplotlib.figure.Figure.get_constrained_layout() \
function Example\n\n', fontweight ="bold")

plt.show()
```

**输出:**

![](img/49fb7c0510440278cb1415d8680f9c94.png)

```py
Value return by get_constrained_layout() : False

```

**例 2:**

```py
# Implementation of matplotlib function
import matplotlib.pyplot as plt
import numpy as np
from matplotlib.patches import Ellipse

NUM = 200

ells = [Ellipse(xy = np.random.rand(2) * 10,
                width = np.random.rand(), 
                height = np.random.rand(),
                angle = np.random.rand() * 360)
        for i in range(NUM)]

fig, ax = plt.subplots(subplot_kw ={'aspect': 'equal'})
for e in ells:
    ax.add_artist(e)
    e.set_clip_box(ax.bbox)
    e.set_alpha(np.random.rand())
    e.set_facecolor(np.random.rand(4))

ax.set_xlim(3, 7)
ax.set_ylim(3, 7)

print("Value return by get_constrained_layout() :",
       fig.get_constrained_layout())

fig.suptitle('matplotlib.figure.Figure.get_constrained_layout() \
function Example\n\n', fontweight ="bold")

plt.show()
```

**输出:**

![](img/8cb02fcfa9bb988d565b68b4cbb729d2.png)

```py
Value return by get_constrained_layout() : False

```
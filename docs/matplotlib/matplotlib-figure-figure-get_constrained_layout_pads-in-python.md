# Python 中的 matplotlib . figure . figure . get _ constrained _ layout _ pads()

> 原文:[https://www . geesforgeks . org/matplotlib-figure-figure-get _ constraint _ layout _ pads-in-python/](https://www.geeksforgeeks.org/matplotlib-figure-figure-get_constrained_layout_pads-in-python/)

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**人物模块**提供了顶级的艺术家，人物，包含了所有的剧情元素。该模块用于控制所有情节元素的子情节和顶层容器的默认间距。

## matplotlib . figure . figure . get _ constraint _ layout _ pads()方法

**matplotlib 库图形模块的 get _ constrained _ layout _ pads()方法**用于获取 constraint _ layout 的填充。

> **语法:** get_constrained_layout_pads(自身，相对=False)
> 
> **参数:**此方法不接受任何参数。
> 
> **返回:**该方法返回 w_pad、h_pad(以英寸为单位)以及 wspace 和 hspace(作为子图的一部分)的列表。

下面的例子说明了 matplotlib.figure . get _ constraint _ layout _ pads()函数在 matplotlib . figure 中的作用:

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

print("Value return by get_constrained_layout_pads() ")
w = list(fig.get_constrained_layout_pads())

print("w_pad :", w[0])
print("h_pad  :", w[1])
print("wspace  :", w[2])
print("hspace  :", w[3])

fig.suptitle('matplotlib.figure.Figure.get_constrained_layout_pads() \
function Example\n\n', fontweight ="bold")

plt.show()
```

**输出:**

![](img/766ae5d878595d8976234a918e86d31b.png)

```py
Value return by get_constrained_layout_pads() 
w_pad : 0.04167
h_pad  : 0.04167
wspace  : 0.02
hspace  : 0.02

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

print("Value return by get_constrained_layout_pads() ")
w = list(fig.get_constrained_layout_pads())

print("w_pad :", w[0])
print("h_pad  :", w[1])
print("wspace  :", w[2])
print("hspace  :", w[3])

fig.suptitle('matplotlib.figure.Figure.get_constrained_layout_pads() \
function Example\n\n', fontweight ="bold")

plt.show()
```

**输出:**

![](img/c6c0e9415bb84726b6c14eb05da0456a.png)

```py
Value return by get_constrained_layout_pads() 
w_pad : 0.04167
h_pad  : 0.04167
wspace  : 0.02
hspace  : 0.02

```
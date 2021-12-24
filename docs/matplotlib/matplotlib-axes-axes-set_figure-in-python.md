# Python 中的 matplotlib . axes . axes . set _ figure()

> 原文:[https://www . geeksforgeeks . org/matplotlib-axes-axes-set _ figure-in-python/](https://www.geeksforgeeks.org/matplotlib-axes-axes-set_figure-in-python/)

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**轴类**包含了大部分的图形元素:轴、刻度、线二维、文本、多边形等。，并设置坐标系。Axes 的实例通过回调属性支持回调。

## matplotlib . axes . axes . set _ figure()函数

matplotlib 库的 axes 模块中的 **Axes.set_figure()函数**用于设置该 Axes 的 figure。

> **语法:**axes . set _ fig(self，fig)
> 
> **参数:**该方法只接受一个参数。
> 
> *   **fig :** 此参数为 fig 实例。
> 
> **返回:**该方法不返回值。

下面的例子说明了 matplotlib.axes . axes . set _ figure()函数在 matplotlib . axes 中的作用:

**例 1:**

```
# Implementation of matplotlib function
import numpy as np
import matplotlib.pyplot as plt
import matplotlib.lines as lines
import matplotlib.transforms as mtransforms
import matplotlib.text as mtext

class GFGfun(lines.Line2D):
    def __init__(self, *args, **kwargs):
        self.text = mtext.Text(0, 0, '')
        lines.Line2D.__init__(self, *args, **kwargs)
        self.text.set_text(self.get_label())

    def set_figure(self, figure):
        self.text.set_figure(figure)
        lines.Line2D.set_figure(self, figure)

    def set_axes(self, axes):
        self.text.set_axes(axes)
        lines.Line2D.set_axes(self, axes)

    def set_transform(self, transform):
        # 2 pixel offset
        texttrans = transform + mtransforms.Affine2D().translate(2, 2)
        self.text.set_transform(texttrans)
        lines.Line2D.set_transform(self, transform)

    def set_data(self, x, y):
        if len(x):
            self.text.set_position((x[-1], y[-1]))

        lines.Line2D.set_data(self, x, y)

    def draw(self, renderer):
        lines.Line2D.draw(self, renderer)
        self.text.draw(renderer)

np.random.seed(10**7)

fig, ax = plt.subplots()
x, y = np.random.rand(2, 20)
line = GFGfun(x, y, mfc ='green',
              ms = 12, 
              label ='Label')

line.text.set_color('green')
line.text.set_fontsize(16)

ax.add_line(line)

fig.suptitle('matplotlib.axes.Axes.set_figure() \
function Example\n\n', fontweight ="bold")

plt.show()
```

**输出:**
![](img/c214d30ff25fdb983dfb022c64fd00ae.png)

**例 2:**

```
# Implementation of matplotlib function
import numpy as np
import matplotlib.pyplot as plt
import matplotlib.lines as lines
import matplotlib.transforms as mtransforms
import matplotlib.text as mtext

class GFGfun(lines.Line2D):
    def __init__(self, *args, **kwargs):
        self.text = mtext.Text(0, 0, '')
        lines.Line2D.__init__(self, *args, **kwargs)
        self.text.set_text(self.get_label())

    def set_figure(self, figure):
        self.text.set_figure(figure)
        lines.Line2D.set_figure(self, figure)

np.random.seed(10**7)

fig, ax = plt.subplots()
x, y = np.random.rand(2, 10)
line = GFGfun(x, y, mfc ='green',
              ms = 12,
              label ='Label')

line.text.set_color('green')
line.text.set_fontsize(16)

ax.add_line(line)

fig.suptitle('matplotlib.axes.Axes.set_figure() \
function Example\n\n', fontweight ="bold")

plt.show()
```

**输出:**
![](img/a8181e0f412c3a275b13b8bc5f6f751b.png)
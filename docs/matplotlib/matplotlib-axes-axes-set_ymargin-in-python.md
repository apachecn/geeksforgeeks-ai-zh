# Python 中的 matplotlib . axes . axes . set _ ymargin()

> 原文:[https://www . geeksforgeeks . org/matplotlib-axes-axes-set _ ymargin-in-python/](https://www.geeksforgeeks.org/matplotlib-axes-axes-set_ymargin-in-python/)

[**Matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**轴类**包含了大部分的图形元素:轴、刻度、线二维、文本、多边形等。，并设置坐标系。Axes 的实例通过回调属性支持回调。

matplotlib.axes.Axes.set_ymargin() Function

matplotlib 库的 Axes 模块中的 **Axes.set_ymargin()函数**用于在自动缩放之前设置 Y 数据限制的填充。

> **语法:** Axes.set_ymargin(self，m)
> **参数:**此方法接受以下参数。
> 
> *   **m:** 此参数用于指定 y 轴的边距值。
> 
> **返回值:**此方法不返回值。

以下示例说明了 matplotlib . axes . axes . set _ ymargin()函数在 matplotlib.axes:
**示例 1:**

## 蟒蛇 3

```py
# Implementation of matplotlib function 
import numpy as np
import matplotlib.pyplot as plt
from matplotlib.widgets import Slider, Button, RadioButtons

fig, (ax, ax1) = plt.subplots(1, 2)
plt.subplots_adjust(bottom = 0.25)
t = np.arange(0.0, 1.0, 0.001)
a0 = 5
f0 = 3
delta_f = 5.0
s = a0 * np.sin(2 * np.pi * f0 * t)
ax.plot(t, s, lw = 2, color = 'green')

ax1.plot(t, s, lw = 2, color = 'green')
ax1.set_ymargin(0.5)

ax.set_title("Without set_ymargin() Function")
ax1.set_title("With set_ymargin value = 0.5")

fig.suptitle('matplotlib.axes.Axes.set_ymargin() \
function Example\n', fontweight ="bold")
fig.canvas.draw()
plt.show()
```

**输出:**

![](img/29e85f7a4a204674f07c8502f9f3ecb5.png)

**例 2:**

## 蟒蛇 3

```py
# Implementation of matplotlib function 
import numpy as np
import matplotlib.pyplot as plt

t = np.arange(0, 3, 1)
t1 = np.cos(np.pi * t) + np.sin(np.pi * t)

fig, [ax1, ax2, ax3] = plt.subplots(nrows = 3)
ax1.plot(t1, color ="green")
ax1.text(0.75, 0.65, 'Original window')

ax2.set_ymargin(2)
ax2.plot(t1, color ="green")
ax2.text(0.8, 3, 'Zoomed out')

ax3.set_ymargin(-0.45)
ax3.plot(t1, color ="green")
ax3.text(0.8, 0.05, 'Zoomed in')

fig.suptitle('matplotlib.axes.Axes.set_ymargin() \
function Example\n', fontweight ="bold")
fig.canvas.draw()
plt.show()
```

**输出:**

![](img/5c2e5f6c8f4d66e10f9c10cb7bab0b12.png)
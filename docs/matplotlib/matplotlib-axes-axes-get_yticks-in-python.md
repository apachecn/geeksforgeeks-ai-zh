# matplotlib . axes . get _ yt wick()用 Python

表示

> 原文:[https://www . geeksforgeeks . org/matplotlib-axes-axes-get _ yticks-in-python/](https://www.geeksforgeeks.org/matplotlib-axes-axes-get_yticks-in-python/)

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**轴类**包含了大部分的图形元素:轴、刻度、线二维、文本、多边形等。，并设置坐标系。Axes 的实例通过回调属性支持回调。

## matplotlib . axes . axes . get _ yticks()函数

matplotlib 库的 Axes 模块中的 **Axes.get_yticks()函数**用于将 y 刻度作为位置列表返回。

> **语法:** Axes.get_yticks(self，minor=False)
> 
> **参数:**该方法接受以下参数。
> 
> *   **次要:**此参数用于设置主要刻度还是次要刻度
> 
> **返回值:**此方法不返回值

下面的例子说明了 matplotlib.axes . axes . get _ yticks()函数在 matplotlib . axes 中的作用:

**例 1:**

```py
# Implementation of matplotlib function
import matplotlib.pyplot as plt
import matplotlib.transforms as mtransforms

fig, ax = plt.subplots()
ax.plot(range(12, 24), range(12))
ax.set_yticks((2, 5, 7, 10))

w = ax.get_yticks()
ax.text(15, 9, "ytick values : "+str(w), 
       fontweight ="bold")

fig.suptitle('matplotlib.axes.Axes.get_yticks() \
function Example\n\n', fontweight ="bold")
plt.show()
```

**输出:**
![](img/76e636e852e05b29267e0f2651814473.png)

**例 2:**

```py
# Implementation of matplotlib function
import matplotlib.pyplot as plt
import numpy as np
import matplotlib.mlab as mlab
import matplotlib.gridspec as gridspec

fs = 1000
t = np.linspace(0, 0.3, 301)
A = np.array([2, 8]).reshape(-1, 1)
f = np.array([150, 140]).reshape(-1, 1)
xn = (A * np.sin(2 * np.pi * f * t)).sum(axis = 0)
xn += 5 * np.random.randn(*t.shape)

fig, ax = plt.subplots()

yticks = np.arange(-50, 30, 10)

ax.psd(xn, NFFT = 301,
       Fs = fs, 
       window = mlab.window_none, 
       pad_to = 1024,
        scale_by_freq = True)

ax.set_yticks(yticks)
ax.grid(True)

w = ax.get_yticks()
ax.text(80, 12, "ytick values : "+str(w), 
        fontweight ="bold")

fig.suptitle('matplotlib.axes.Axes.get_yticks() \
function Example\n\n', fontweight ="bold")
plt.show()
```

**输出:**
![](img/2fbfbb78789bf6ae87887b283f2cab92.png)
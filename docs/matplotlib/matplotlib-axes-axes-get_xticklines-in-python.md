# matplotlib . axes . get _ xticklines()用 Python

表示

> 原文:[https://www . geeksforgeeks . org/matplotlib-axes-axes-get _ xticklines-in-python/](https://www.geeksforgeeks.org/matplotlib-axes-axes-get_xticklines-in-python/)

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**轴类**包含了大部分的图形元素:轴、刻度、线二维、文本、多边形等。，并设置坐标系。Axes 的实例通过回调属性支持回调。

## matplotlib . axes . axes . get _ xticklines()函数

matplotlib 库的 Axes 模块中的 **Axes.get_xticklines()函数**用于将 x 刻度线作为 Line2D 实例的列表返回。

> **语法:** Axes.get_xticklines(self)
> 
> **参数:**该方法不接受任何参数。
> 
> **返回值:**该方法返回 x 条刻度线作为线 2D 实例列表。

下面的例子说明了 matplotlib.axes . axes . get _ xticklines()函数在 matplotlib . axes 中的作用:

**例 1:**

```
# Implementation of matplotlib function
import numpy as np
import matplotlib.pyplot as plt
from matplotlib.patches import Polygon

def func(x):
    return (x - 4) * (x - 6) * (x - 5) + 100

a, b = 2, 9  # integral limits
x = np.linspace(0, 10)
y = func(x)

fig, ax = plt.subplots()
ax.plot(x, y, "k", linewidth = 2)
ax.set_ylim(bottom = 0)

# Make the shaded region
ix = np.linspace(a, b)
iy = func(ix)
verts = [(a, 0), *zip(ix, iy), (b, 0)]
poly = Polygon(verts, facecolor ='green',
               edgecolor ='0.5', alpha = 0.4)
ax.add_patch(poly)

ax.text(0.5 * (a + b), 30,
        r"$\int_a ^ b f(x)\mathrm{d}x{content}quot;,
        horizontalalignment ='center', 
        fontsize = 20)

fig.text(0.9, 0.05, '$x{content}apos;)
fig.text(0.1, 0.9, '$y{content}apos;)

ax.spines['right'].set_visible(False)
ax.spines['top'].set_visible(False)

ax.set_xticks((a, b-a, b))
ax.set_xticklabels(('$a{content}apos;, '$valx{content}apos;, '$b{content}apos;))

w = ax.get_xticklines()
ax.text(3, 200, "xticklines values : ", 
       fontweight ="bold")
xx = 200
for i in w:
    ax.text(4, xx-15, str(i), fontweight ="bold")
    xx-= 15

fig.suptitle('matplotlib.axes.Axes.get_xticklines()\
 function Example\n\n', fontweight ="bold")
fig.canvas.draw()
plt.show()
```

**输出:**
![](img/2e70a83c61ddd5a15de4044fc70941f5.png)

**例 2:**

```
# Implementation of matplotlib function
import numpy as np
import matplotlib.pyplot as plt

# Fixing random state for reproducibility
np.random.seed(19680801)

x = np.linspace(0, 2 * np.pi, 100)
y = np.sin(x)
y2 = y + 0.2 * np.random.normal(size = x.shape)

fig, ax = plt.subplots()
ax.plot(x, y)
ax.plot(x, y2)

ax.set_xticks([0, np.pi, 2 * np.pi])
ax.set_xticklabels(['0', r'$pi{content}apos;, r'2$pi{content}apos;])

ax.spines['left'].set_bounds(-1, 1)
ax.spines['right'].set_visible(False)
ax.spines['top'].set_visible(False)

w = ax.get_xticklines()
ax.text(2, 0.8, "xticklines values : ", 
        fontweight ="bold")
xx = 0.8
for i in w:
    ax.text(2.3, xx-0.2, str(i), fontweight ="bold")
    xx-= 0.2

fig.suptitle('matplotlib.axes.Axes.get_xticklines() \
function Example\n\n', fontweight ="bold")
fig.canvas.draw()
plt.show()
```

**输出:**
![](img/b9705127867873684699d37a7687ff7b.png)
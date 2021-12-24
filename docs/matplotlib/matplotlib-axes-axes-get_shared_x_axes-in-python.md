# Python 中的 matplotlib . axes . axes . get _ shared _ x _ axes()

> 原文:[https://www . geeksforgeeks . org/matplotlib-axes-axes-get _ shared _ x _ axes-in-python/](https://www.geeksforgeeks.org/matplotlib-axes-axes-get_shared_x_axes-in-python/)

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**轴类**包含了大部分的图形元素:轴、刻度、线二维、文本、多边形等。，并设置坐标系。Axes 的实例通过回调属性支持回调。

## matplotlib . axes . axes . get _ shared _ x _ axes()函数

matplotlib 库的 Axes 模块中的**Axis . get _ shared _ x _ axes()函数**用于返回 x 轴的共享轴 Grouper 对象的引用。

**语法:**

```
Axes.get_shared_x_axes(self)

```

下面的例子说明了 matplotlib.axes . axes . get _ shared _ x _ axes()函数在 matplotlib . axes 中的作用:

**例 1:**

```
# Implementation of matplotlib function
import matplotlib.pyplot as plt
import numpy as np

def GFG1(temp):
    return (5\. / 9.) * (temp - 32)

def GFG2(ax1):
    y1, y2 = ax1.get_ylim()
    ax_twin .set_ylim(GFG1(y1), GFG1(y2))
    ax_twin .figure.canvas.draw()

fig, ax1 = plt.subplots()
ax_twin = ax1.twinx()

ax1.callbacks.connect("ylim_changed", GFG2)
ax1.plot(np.linspace(-40, 120, 100))
ax1.set_xlim(0, 100)

ax1.set_ylabel('Fahrenheit')
ax_twin .set_ylabel('Celsius')

w = ax1.get_shared_x_axes()
w1 = ax_twin.get_shared_x_axes()
for i in w:
    x, y = list(i)
    ax1.text(40, 100, "Value return : \n",
            fontweight ="bold")
    ax1.text(27, 90, str(x)+"\n"+str(y), 
             fontweight ="bold")
fig.suptitle('matplotlib.axes.Axes.get_shared_x_axes()\
 function Example\n\n', fontweight ="bold")
plt.show()
```

**输出:**
![](img/fb7034662da6da637ebe653f4aff1a25.png)

**例 2:**

```
# Implementation of matplotlib function
import numpy as np
import matplotlib.pyplot as plt

# Create some mock data
t = np.arange(0.01, 10.0, 0.001)
data1 = np.exp(t)
data2 = np.sin(0.4 * np.pi * t)

fig, ax1 = plt.subplots()

color = 'tab:blue'
ax1.set_xlabel('time (s)')
ax1.set_ylabel('exp', color = color)
ax1.plot(t, data1, color = color)
ax1.tick_params(axis ='y', labelcolor = color)

ax2 = ax1.twinx()

color = 'tab:green'
ax2.set_ylabel('sin', color = color)
ax2.plot(t, data2, color = color)
ax2.tick_params(axis ='y', labelcolor = color)

w = ax1.get_shared_x_axes()
w1 = ax2.get_shared_x_axes()
for i in w:
    x, y = list(i)
    ax1.text(4, 15000, "Value return : \n", 
             fontweight ="bold")
    ax1.text(2, 13000, str(x)+"\n"+str(y),
             fontweight ="bold")
fig.suptitle('matplotlib.axes.Axes.get_shared_x_axes()\
 function Example\n\n', fontweight ="bold")
plt.show()
```

**输出:**
![](img/26cd27371ce44ca0070e1c56bf9e8b1c.png)
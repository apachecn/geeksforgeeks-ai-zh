# matplotlib.axes.Axes.twiny()在 Python

中

> 哎哎哎:# t0]https://www . geeksforgeeks . org/matplot lib-axes-twiny-in-python/

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**轴类**包含了大部分的图形元素:轴、刻度、线二维、文本、多边形等。，并设置坐标系。Axes 的实例通过回调属性支持回调。

## matplotlib.axes.Axes.twiny()函数

matplotlib 库的 axes 模块中的 **Axes.twiny()函数**用于创建一个共享 yaxis 的双 Axes。

> **语法:**轴.孪生(自)
> 
> **返回值:**该方法用于返回以下内容。
> 
> *   **ax_twin :** 这将返回新创建的 Axes 实例。

下面的例子说明了 matplotlib.axes.Axes.twiny()函数在 matplotlib.axes 中的作用:

**例 1:**

```py
# Implementation of matplotlib function
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
ax_twin = ax1.twiny()

ax1.callbacks.connect("ylim_changed", GFG2)
ax1.plot(np.linspace(-40, 120, 100))
ax1.set_ylim(0, 100)

ax1.set_xlabel('Fahrenheit')
ax_twin .set_xlabel('Celsius')

fig.suptitle('matplotlib.axes.Axes.twiny()\
 function Example\n\n', fontweight ="bold")
plt.show()
```

**输出:**
![](img/63686996c49a514d61deba8ecfa8105a.png)

**例 2:**

```py
# Implementation of matplotlib function
import numpy as np
import matplotlib.pyplot as plt

# Create some mock data
t = np.arange(0.01, 10.0, 0.001)
data1 = np.exp(t)
data2 = np.sin(0.4 * np.pi * t)

fig, ax1 = plt.subplots()

color = 'tab:blue'
ax1.set_ylabel('time (s)')
ax1.set_xlabel('exp', color = color)
ax1.plot(data1, t, color = color)
ax1.tick_params(axis ='x', labelcolor = color)

ax2 = ax1.twiny()

color = 'tab:green'
ax2.set_xlabel('sin', color = color)
ax2.plot(data2, t, color = color)
ax2.tick_params(axis ='x', labelcolor = color)

fig.suptitle('matplotlib.axes.Axes.twiny()\
 function Example\n\n', fontweight ="bold")
plt.show()
```

**输出:**
![](img/8f6d25b19acb0652a291ca7662c69194.png)
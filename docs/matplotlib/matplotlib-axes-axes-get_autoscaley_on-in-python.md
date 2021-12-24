# Python 中的 matplotlib . axes . axes . get _ autoscaley _ on()

> 原文:[https://www . geeksforgeeks . org/matplotlib-axes-axes-get _ autoscaley _ on-in-python/](https://www.geeksforgeeks.org/matplotlib-axes-axes-get_autoscaley_on-in-python/)

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**轴类**包含了大部分的图形元素:轴、刻度、线二维、文本、多边形等。，并设置坐标系。Axes 的实例通过回调属性支持回调。

## matplotlib . axes . axes . get _ autoscaley _ on()函数

matplotlib 库的 Axes 模块中的**Axis . get _ autoscaley _ on()函数**用于获取 y 轴的自动缩放是否应用于绘图命令。

> **语法:** Axes.get_autoscaley_on(self)
> 
> **参数:**该方法不接受任何参数。
> 
> **返回值:**该方法返回布尔值。

下面的例子说明了 matplotlib.axes . axes . get _ autoscaley _ on()函数在 matplotlib . axes 中的作用:

**例 1:**

```
# ImpleIn Reviewtation of matplotlib function  
import numpy as np
import matplotlib.pyplot as plt

t = np.linspace(0, 20, 300)
xdata = np.sin(np.pi * t / 12)
ydata = np.cos(4 * np.pi * t / 21)

fig, ax = plt.subplots()

ax.plot(xdata, ydata, 'g-')
w = ax.get_autoscaley_on()
ax.text(-0.5, -0.75, "Value return by get_autoscaley_on : "
        + str(w),
        fontweight ="bold")
fig.suptitle('matplotlib.axes.Axes.get_autoscaley_on() function \
Example\n', fontweight ="bold")
fig.canvas.draw()
plt.show()
```

**输出:**
![](img/ea2cb8384393b8966ff8d866db5473d3.png)

**例 2:**

```
# ImpleIn Reviewtation of matplotlib function  
import numpy as np
import matplotlib.pyplot as plt

t = np.linspace(16, 365, (365-16)*4)
xdata = np.sin(2 * np.pi * t / 15)
ydata = np.cos(2 * np.pi * t / 12)

fig, (ax, ax1) = plt.subplots(1, 2)

ax.plot(xdata, ydata, 'g-', alpha = 0.6)
ax.set_title("Axes 1")
ax1.plot(xdata, ydata, 'g-', alpha = 0.6)
ax1.set_autoscaley_on(False)
ax1.set_title("Axes 2")

w = ax.get_autoscaley_on()
w1 = ax1.get_autoscaley_on()
ax.text(-0.5, 0, "Value return : " + str(w),
        fontweight ="bold")
ax1.text(-0.5, 0.5, "Value return : " + str(w1),
         fontweight ="bold")

fig.suptitle('matplotlib.axes.Axes.get_autoscaley_on() \
function Example\n', fontweight ="bold")
fig.canvas.draw()
plt.show()
```

**输出:**
![](img/509f4c8cbc91a5e67031d131390ee6e4.png)
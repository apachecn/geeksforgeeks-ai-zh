# Matplotlib.pyplot.twinx()在 Python

中

> 哎哎哎:# t0]https://www . geeksforgeeks . org/matplot lib-pyplot-twinx-in-python/

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。 **[Pyplot](https://www.geeksforgeeks.org/pyplot-in-matplotlib/)** 是一个基于状态的接口到 **Matplotlib** 模块，它提供了一个类似于 MATLAB 的接口。

**样本代码**

```py
# sample code
import matplotlib.pyplot as plt 

plt.plot([1, 2, 3, 4], [16, 4, 1, 8]) 
plt.show() 
```

**输出:**
![](img/318b2f71555c93680d9f59450380bc8c.png)

## matplotlib.pyplot.twinx()函数

matplotlib 库 pyplot 模块中的 **twinx()函数**用于制作和返回共享 x 轴的第二个轴。

> **语法:**
> 
> ```py
> matplotlib.pyplot.twinx(ax=None)
> ```
> 
> **参数:**该方法不接受任何参数。
> 
> **返回:**返回共享 x 轴的第二个轴

下面的例子说明了 matplotlib.pyplot.twinx()函数在 matplotlib.pyplot 中的作用:

**示例#1:**

```py
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
ax1.plot(np.linspace(0, 120, 100))
ax1.set_xlim(30, 100)

ax1.set_ylabel('Fahrenheit')
ax_twin .set_ylabel('Celsius')

fig.suptitle('matplotlib.pyplot.twinx() function \
Example\n\n', fontweight ="bold")
plt.show()
```

**输出:**
![](img/230b4921e28a701a22af143a30530621.png)

**例 2:**

```py
# Implementation of matplotlib function
import numpy as np
import matplotlib.pyplot as plt

# Create some mock data
t = np.arange(0.01, 20.0, 0.001)
data1 = np.exp(t)
data2 = np.sin(0.3 * np.pi * t)

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

fig.suptitle('matplotlib.pyplot.twinx() function \
Example\n\n', fontweight ="bold")
plt.show()
```

**输出:**
![](img/1768fc4d52a052b64caf1234469e9be1.png)
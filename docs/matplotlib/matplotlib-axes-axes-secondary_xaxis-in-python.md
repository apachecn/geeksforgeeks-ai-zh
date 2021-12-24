# Python 中的 matplotlib . axes . axes . secondary _ xaxis()

> 原文:[https://www . geeksforgeeks . org/matplotlib-axes-axes-secondary _ xaxis-in-python/](https://www.geeksforgeeks.org/matplotlib-axes-axes-secondary_xaxis-in-python/)

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**轴类**包含了大部分的图形元素:轴、刻度、线二维、文本、多边形等。，并设置坐标系。Axes 的实例通过回调属性支持回调。

## matplotlib . axes . axes . secondary _ xaxis()函数

matplotlib 库的 Axes 模块中的**axes . second _ xaxis()函数**也用于给该轴添加第二个 x 轴。

> **语法:** Axes.secondary_xaxis(self，location，* functions = None，**kwargs)
> 
> **参数:**该方法接受以下描述的参数:
> 
> *   **位置:**该参数是放置副轴的位置。
> *   **函数:**该参数用于指定变换函数及其逆函数。
> 
> **返回:**该方法返回以下内容:
> 
> *   **斧:**此回 ***斧。_ 副轴。**次级亚星*。

**注意:**该功能在 Matplotlib 版本>中工作= 3.1

下面的例子说明了 matplotlib.axes . axes . secondary _ xaxis()函数在 matplotlib . axes 中的作用:

**例 1:**

```py
# Implementation of matplotlib function
import matplotlib.pyplot as plt
import numpy as np

fig, ax = plt.subplots()
ax.plot([1, 2, 3])

ax.set_xlabel('X-Axis')
ax.set_ylabel('Y-Axis')

secax = ax.secondary_xaxis('top')
secax.set_xlabel('Secondary-X-Axis')
ax.set_title('matplotlib.axes.Axes.secondary_xaxis() Example',
             fontsize = 14, fontweight ='bold')
plt.show()
```

**输出:**
![](img/5157b54c4895978fc0242dbc731ac47c.png)

**例 2:**

```py
# Implementation of matplotlib function
import matplotlib.pyplot as plt
import numpy as np
import datetime
import matplotlib.dates as mdates
from matplotlib.transforms import Transform
from matplotlib.ticker import (
    AutoLocator, AutoMinorLocator)

fig, ax = plt.subplots(constrained_layout = True)
x = np.arange(0, 500, 2)
y = np.sin(3 * x * np.pi / 180)
ax.plot(x, y)
ax.set_xlabel('Degree')
ax.set_ylabel('Frequency')

def val1(x):
    return x * np.pi / 180

def val2(x):
    return x * 180 / np.pi

secax = ax.secondary_xaxis('top', functions =(val1, val2))
secax.set_xlabel('Radian')
ax.set_title('matplotlib.axes.Axes.secondary_xaxis() Example',
             fontsize = 14, fontweight ='bold')
plt.show()
```

**输出:**
![](img/fd0ee8e6307aeb1649b8e14259e08b24.png)
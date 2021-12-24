# Python 中的 matplotlib . fig . fig . get _ fig height()

> 原文:[https://www . geesforgeks . org/matplotlib-fig-fig-fig-height-in-python/](https://www.geeksforgeeks.org/matplotlib-figure-figure-get_figheight-in-python/)

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**人物模块**提供了顶级的艺术家，人物，包含了所有的剧情元素。该模块用于控制所有情节元素的子情节和顶层容器的默认间距。

## matplotlib . fig . fig . get _ fig height()方法

**利用 matplotlib 库的 get_figheight()方法**图形模块将图形高度作为一个浮点数获取。

> **语法:** get_figheight(self)
> 
> **参数:**此方法不接受任何参数。
> 
> **返回:**该方法以浮点数形式返回图形高度。

下面的例子说明了 matplotlib.figure . fig . get _ fig height()函数在 matplotlib . fig:

**例 1:**

```py
# Implementation of matplotlib function 
import matplotlib.pyplot as plt 
from matplotlib.figure import Figure
from mpl_toolkits.axisartist.axislines import Subplot 
import numpy as np 

fig = plt.figure() 

ax = Subplot(fig, 111) 
fig.add_subplot(ax)  

w = fig.get_figheight()
ax.text(0.2, 0.5,
        "Value Return by get_figheight() : "
        + str(w),
        fontweight ="bold")

fig.canvas.draw()
fig.suptitle('matplotlib.figure.Figure.get_figheight()\
function Example', fontweight ="bold") 

plt.show()
```

**输出:**
![](img/9d1bd7e44eb3d063fb16a5a31aff530e.png)

**例 2:**

```py
# Implementation of matplotlib function 
import matplotlib.pyplot as plt 
from matplotlib.figure import Figure
import numpy as np

fig = plt.figure(edgecolor = "red", figsize =(7, 6)) 

ax = fig.add_axes([0.1, 0.1, 0.8, 0.8])

xx = np.arange(0, 2 * np.pi, 0.01) 
ax.plot(xx, np.sin(xx)) 

w = fig.get_figheight()
ax.text(1.5, 0,
        "Value Return by get_figheight() : "
        + str(w),
        fontweight ="bold")

fig.canvas.draw()

fig.suptitle('matplotlib.figure.Figure.get_figheight()\
function Example', fontweight ="bold") 

plt.show()
```

**输出:**
![](img/1eff1c91176f4c8af01c9cdff8ab896b.png)
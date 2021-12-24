# Python 中的 matplotlib . figure . figure . get _ frame on()

> 原文:[https://www . geesforgeks . org/matplotlib-figure-figure-get _ frame on-in-python/](https://www.geeksforgeeks.org/matplotlib-figure-figure-get_frameon-in-python/)

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**人物模块**提供了顶级的艺术家，人物，包含了所有的剧情元素。该模块用于控制所有情节元素的子情节和顶层容器的默认间距。

## matplotlib . figure . figure . get _ frame on()方法

**利用 matplotlib 库的 get_frameon()方法**图形模块获取图形的背景面片可见性。

> **语法:** get_frameon(self)
> 
> **参数:**此方法不接受任何参数。
> 
> **返回:**该方法返回人物的背景补丁可见性。

下面的例子说明了 matplotlib.figure . figure . get _ frame on()函数在 matplotlib . figure 中的作用:

**例 1:**

```
# Implementation of matplotlib function 
import matplotlib.pyplot as plt 
from matplotlib.figure import Figure
from mpl_toolkits.axisartist.axislines import Subplot 
import numpy as np 

fig = plt.figure() 

ax = Subplot(fig, 111) 
fig.add_subplot(ax)  

w = fig.get_frameon()
ax.text(0.2, 0.5,
        "Value Return by get_frameon() : "
        + str(w),
        fontweight ="bold")

fig.canvas.draw()
fig.suptitle('matplotlib.figure.Figure.get_frameon()\
function Example', fontweight ="bold") 

plt.show()
```

**输出:**
![](img/9578119971d84e0102699d72f625db83.png)

**例 2:**

```
# Implementation of matplotlib function 
import matplotlib.pyplot as plt 
from matplotlib.figure import Figure
import numpy as np 

fig = plt.figure(edgecolor = "red", figsize =(7, 6)) 

ax = fig.add_axes([0.1, 0.1, 0.8, 0.8])

xx = np.arange(0, 2 * np.pi, 0.01) 
ax.plot(xx, np.sin(xx)) 

w = fig.get_frameon()
ax.text(1.5, 0,
        "Value Return by get_frameon() : "
        + str(w),
        fontweight ="bold")

fig.canvas.draw()

fig.suptitle('matplotlib.figure.Figure.get_frameon() \
function Example', fontweight ="bold") 

plt.show()
```

**输出:**
![](img/f83ca61e1ef396cc8b32575d876efb27.png)
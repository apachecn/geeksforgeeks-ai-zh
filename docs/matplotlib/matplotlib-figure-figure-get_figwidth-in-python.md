# Python 中的 matplotlib . fig . fig . get _ fig width()

> 原文:[https://www . geeksforgeeks . org/matplotlib-fig-fig-fig-width-in-python/](https://www.geeksforgeeks.org/matplotlib-figure-figure-get_figwidth-in-python/)

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**人物模块**提供了顶级的艺术家，人物，包含了所有的剧情元素。该模块用于控制所有情节元素的子情节和顶层容器的默认间距。

## matplotlib . fig . fig . get _ fig width()方法

**利用 matplotlib 库的 get_figwidth()方法**图形模块，将图形宽度作为浮点数获取。

> **语法:** get_figwidth(self)
> 
> **参数:**此方法不接受任何参数。
> 
> **返回:**该方法以浮点数形式返回图形宽度。

下面的例子说明了 matplotlib.figure . fig . get _ fig width()函数在 matplotlib . fig:

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

w = fig.get_figwidth()
ax.text(0.2, 0.5, 
        "Value Return by get_figwidth() : "
        + str(w),
        fontweight ="bold")

fig.canvas.draw()
fig.suptitle('matplotlib.figure.Figure.get_figwidth() \
function Example', fontweight ="bold") 

plt.show()
```

**输出:**

![get_figwidth-matplotlib](img/724271e500bcceaa4e4a3790fcca5a58.png)

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

w = fig.get_figwidth()
ax.text(1.5, 0,
        "Value Return by get_figwidth() : "
        + str(w),
        fontweight ="bold")

fig.canvas.draw()
fig.suptitle('matplotlib.figure.Figure.get_figwidth() \
function Example', fontweight ="bold") 

plt.show()
```

**输出:**

![get_figwidth-python-2](img/a30ae40a2f3a0fdbd75bedd427fdfb5b.png)
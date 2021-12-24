# Python 中的 matplotlib . figure . figure . set _ size _ inches()

> 原文:[https://www . geeksforgeeks . org/matplotlib-figure-figure-set _ size _ inches-in-python/](https://www.geeksforgeeks.org/matplotlib-figure-figure-set_size_inches-in-python/)

[**Matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**人物模块**提供了顶级的艺术家，人物，包含了所有的剧情元素。该模块用于控制所有情节元素的子情节和顶层容器的默认间距。

## matplotlib . figure . figure . set _ size _ inches()方法

matplotlib 库的 **set_size_inches()方法**图形模块用于设置以英寸为单位的图形尺寸。

> **语法:** set_size_inches(self，w，h =无，forward=True)
> 
> **参数:**该方法接受下面讨论的以下参数:
> 
> *   **w，h :** 这些参数是以英寸为单位的图形的(宽度，高度)。
> 
> **返回:**此方法不返回任何值。

下面的例子说明了 matplotlib.figure . figure . set _ size _ inches()函数在 matplotlib . figure 中的作用:

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

fig.set_size_inches(4, 5)

fig.suptitle("""matplotlib.figure.Figure.set_size_inches()
function Example\n\n""", fontweight ="bold") 

plt.show()
```

**输出:**
![](img/33db15d1255754d166e5b0c19fbdb5ea.png)

**例 2:**

```py
# Implementation of matplotlib function 
import matplotlib.pyplot as plt 
from matplotlib.figure import Figure
import numpy as np 

fig = plt.figure(figsize =(7, 6)) 

ax = fig.add_axes([0.1, 0.1, 0.8, 0.8])

xx = np.arange(0, 2 * np.pi, 0.01) 
ax.plot(xx, np.sin(xx)) 

fig.set_size_inches(6, 4)

fig.suptitle("""matplotlib.figure.Figure.set_size_inches()
function Example\n\n""", fontweight ="bold") 

plt.show() 
```

**输出:**
![](img/77a5274c4fcfdb356634f5720ce0a24e.png)
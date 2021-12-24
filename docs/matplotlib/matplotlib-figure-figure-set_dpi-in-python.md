# Python 中的 matplotlib . figure . figure . set _ dpi()

> 原文:[https://www . geesforgeks . org/matplotlib-figure-figure-set _ dpi-in-python/](https://www.geeksforgeeks.org/matplotlib-figure-figure-set_dpi-in-python/)

[**Matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**人物模块**提供了顶级的艺术家，人物，包含了所有的剧情元素。该模块用于控制所有情节元素的子情节和顶层容器的默认间距。

## matplotlib . figure . figure . set _ dpi()方法

matplotlib 库的 **set_dpi()方法**图形模块用于设置图形的分辨率，单位为每英寸点数。

> **语法:** set_dpi(self，val)
> 
> **参数:**该方法接受下面讨论的以下参数:
> 
> *   **val :** 该参数为浮点值。
> 
> **返回:**此方法不返回任何值。

以下示例说明了 matplotlib.figure . figure . set _ dpi()函数在 matplotlib . figure 中的作用:

**例 1:**

```py
# Implementation of matplotlib function 
import matplotlib.pyplot as plt 
from matplotlib.figure import Figure
import numpy as np 

fig = plt.figure(figsize =(5, 4)) 

ax = fig.add_axes([0.1, 0.1, 0.8, 0.8])

xx = np.arange(0, 2 * np.pi, 0.01) 
ax.plot(xx, np.sin(xx)) 

fig.set_dpi(150.0)

fig.suptitle("""matplotlib.figure.Figure.set_dpi()
function Example\n\n""", fontweight ="bold") 

plt.show() 
```

**输出:**
![](img/9b8259138c817922cf982d5730fb0f71.png)

**例 2:**

```py
# Implementation of matplotlib function 
import matplotlib.pyplot as plt 
from matplotlib.figure import Figure
from mpl_toolkits.axisartist.axislines import Subplot 
import numpy as np 

fig = plt.figure(facecolor ="lightgreen") 

ax = Subplot(fig, 111) 
fig.add_subplot(ax) 

ax.axis["left"].set_visible(False) 
ax.axis["top"].set_visible(False)

fig.set_dpi(90.0)

fig.suptitle("""matplotlib.figure.Figure.set_dpi()
function Example\n\n""", fontweight ="bold") 

plt.show() 
```

**输出:**
![](img/249b696fc61afea08e78583287b7c203.png)
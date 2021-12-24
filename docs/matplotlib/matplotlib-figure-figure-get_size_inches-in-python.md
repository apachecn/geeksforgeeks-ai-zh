# Python 中的 matplotlib . figure . figure . get _ size _ inches()

> 原文:[https://www . geesforgeks . org/matplotlib-figure-figure-get _ size _ inches-in-python/](https://www.geeksforgeeks.org/matplotlib-figure-figure-get_size_inches-in-python/)

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**人物模块**提供了顶级的艺术家，人物，包含了所有的剧情元素。该模块用于控制所有情节元素的子情节和顶层容器的默认间距。

## matplotlib . figure . figure . get _ size _ inches()方法

**利用 matplotlib 库的 get_size_inches()方法**图形模块获取当前图形的尺寸，单位为英寸。

> **语法:** get_size_inches(self)
> 
> **参数:**此方法不接受任何参数。
> 
> **返回:**此方法返回以英寸为单位的图形大小(宽、高)。

下面的例子说明了 matplotlib.figure . figure . get _ size _ inches()函数在 matplotlib . figure 中的作用:

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

w = fig.get_size_inches()
ax.text(0.2, 0.5,
        "Value Return by get_size_inches() : "
        + str(w),
        fontweight ="bold")

fig.canvas.draw()

fig.suptitle('matplotlib.figure.Figure.get_size_inches()\
 function Example', fontweight ="bold") 

plt.show()
```

**输出:**
![](img/39224ca2745edce6ffb69f01559a3183.png)

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

w = fig.get_size_inches()
ax.text(1.5, 0,
        "Value Return by get_size_inches() : " 
        + str(w),
        fontweight ="bold")

fig.canvas.draw()

fig.suptitle('matplotlib.figure.Figure.get_size_inches() \
function Example', fontweight ="bold") 

plt.show()
```

**输出:**
![](img/c28f01de2cc59df8ecc85c832c7ef5c5.png)
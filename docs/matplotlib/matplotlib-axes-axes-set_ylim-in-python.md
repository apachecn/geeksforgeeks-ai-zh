# matplotlib . axes . set _ ylim()用 Python

表示

> 哎哎哎:# t0]https://www . geeksforgeeks . org/matplot lib-axes-set _ ylim-in-python/

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**轴类**包含了大部分的图形元素:轴、刻度、线二维、文本、多边形等。，并设置坐标系。Axes 的实例通过回调属性支持回调。

**matplotlib.axes.Axes.set_ylim() Function:**

matplotlib 库的 Axes 模块中的 **Axes.set_ylim()函数**用于设置 y 轴视图限制。

> **语法:** Axes.set_ylim(self，底部=无，顶部=无，发出=真，自动=假，* ymin =无，ymax =无)
> 
> **参数:**该方法接受以下参数。
> 
> *   **底部:**此参数是数据坐标中的底部 ylim
> *   **顶部:**此参数是数据坐标中的顶部 ylim
> *   **发出:**此参数用于通知观察者极限变化。
> *   **自动:**该参数用于开启 x 轴的自动缩放。
> *   **ymin，ymax:** 这些参数相当于底部和顶部，同时传递 ymin 和底部或者 ymax 和顶部都是错误。
> 
> **返回:**该方法返回以下内容
> 
> *   **底部，顶部:**这将返回数据坐标中的新 y 轴限制。

下面的例子说明了 matplotlib.axes.Axes.set_ylim()函数在 matplotlib.axes 中的作用:

**例 1:**

```
# Implementation of matplotlib function
from matplotlib.widgets import Cursor
import numpy as np
import matplotlib.pyplot as plt

np.random.seed(19680801)

fig, ax = plt.subplots(facecolor ='# A0F0CC')

x, y = 4*(np.random.rand(2, 100) - .5)
ax.plot(x, y, 'g')
ax.set_ylim(-3, 3)

cursor = Cursor(ax, useblit = True, color ='red',
                linewidth = 2)

ax.set_title('matplotlib.axes.Axes.set_ylim() Example\n',
             fontsize = 14, fontweight ='bold')
plt.show()
```

**输出:**
![](img/11c6cfb0450f7fe915f100ecd7bee7e8.png)

**例 2:**

```
# Implementation of matplotlib function
import matplotlib.pyplot as plt
import numpy as np

fig1, ax1 = plt.subplots()
fig2, ax2 = plt.subplots()
ax1.set(xlim =(-0.5, 1.5), ylim =(-0.5, 1.5),
               autoscale_on = False)
ax2.set(xlim =(0.5, 0.75), ylim =(0.5, 0.75),
               autoscale_on = False)

x, y, s, c = np.random.rand(4, 200)
s *= 200

ax1.scatter(x, y, s, c)
ax2.scatter(x, y, s, c)

def GFG(event):
    if event.button != 1:
        return
    x, y = event.xdata, event.ydata
    ax2.set_xlim(x - 0.1, x + 0.1)
    ax2.set_ylim(y - 0.1, y + 0.1)
    fig2.canvas.draw()

fig1.canvas.mpl_connect('button_press_event', GFG)   
ax1.set_title('matplotlib.axes.Axes.set_ylim()\
 Example\n Original Window ',
             fontsize = 14, fontweight ='bold')
ax2.set_title('Zoomed window ',
             fontsize = 14, fontweight ='bold')
plt.show()
```

**输出:**
![](img/fe3e5a0c1014ac87c88c874d80954549.png)
![](img/3e57e29652c729575280ea9bce2c0de8.png)
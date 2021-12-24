# matplotlib . axes . fill _ betweenx()用 Python

表示

> 原文:[https://www . geeksforgeeks . org/matplotlib-axes-axes-fill _ between x-in-python/](https://www.geeksforgeeks.org/matplotlib-axes-axes-fill_betweenx-in-python/)

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**轴类**包含了大部分的图形元素:轴、刻度、线二维、文本、多边形等。，并设置坐标系。Axes 的实例通过回调属性支持回调。

## matplotlib . axes . axes . fill _ betwex()函数

matplotlib 库的 Axes 模块中的 **Axes.fill_betweenx()函数**用于填充两条竖曲线之间的区域。

> **语法:** Axes.fill_betweenx(self，y，x1，x2=0，其中=None，step=None，interpolate = False，* data = None，**kwargs)
> 
> **参数:**该方法接受以下描述的参数:
> 
> *   **y:** 该参数包含用于定义曲线的数据点的 y 坐标。
> *   **x1:** 该参数包含用于定义第一条曲线的数据点的 x 坐标
> *   **x2:** 该参数包含用于定义第二条曲线的数据点的 x 坐标。它是可选的，默认值为 0。
> *   **其中:**该参数为可选参数。并且用于排除一些水平区域被填充。
> *   **插值:**该参数也是可选参数。默认值为误差线的线宽*无*。
> *   **步骤:**该参数也是可选参数。它用于定义填充是否应该是阶跃函数。
> 
> **返回:**返回包含绘制多边形的多边形集合。

下面的例子说明了 matplotlib.axes . axes . fill _ between x()函数在 matplotlib . axes 中的作用:

**示例-1:**

```py
# Implementation of matplotlib function

import numpy as np
import matplotlib.pyplot as plt

y = np.arange(-5, 5, 0.01)
x1 = -y * 2 + y + 10
x2 = 2 * y + y

fig, ax = plt.subplots()
ax.plot(y, x1, y, x2, color ='black')
ax.fill_betweenx(y, x1, x2, where = x2 >x1, 
                 facecolor ='green', alpha = 0.8)

ax.fill_betweenx(y, x1, x2, where = x2 <= x1,
                 facecolor ='black', alpha = 0.8)

ax.set_title('matplotlib.axes.Axes.fill_betweenx Example1')
plt.show()
```

**输出:**
![](img/bb1e45978af9051b1a1079ae6426aba2.png)
**例-2:**

```py
# Implementation of matplotlib function

import numpy as np
import matplotlib.pyplot as plt

y = np.arange(0.0, 2, 0.01)
x1 = np.sin(2 * np.pi * y)
x2 = 0.8 * np.sin(4 * np.pi * y)

fig, [ax1, ax2, ax3, ax4] = plt.subplots(1, 4,
                                         sharey = True,
                                         figsize =(6, 6))

ax1.fill_betweenx(y, 0, x1, facecolor ='green')
ax1.set_title('Fill_Betweenx x1 and 0')

ax2.fill_betweenx(y, x1, 1, facecolor ='green')
ax2.set_title('Fill_Betweenx x1 and 1')

ax3.fill_betweenx(y, x1, x2, facecolor ='green')
ax3.set_title('Fill_Betweenx x1 and y2')

ax4.fill_betweenx(y, x1, x2, where = x2 <= x1, 
                  facecolor ='green')

ax4.set_title('Fill_Between x1 and x2 with x2<= x1 ' )
plt.show()
```

**输出:**
![](img/f6c322cbb701a63b4aa01602ee32dfe4.png)
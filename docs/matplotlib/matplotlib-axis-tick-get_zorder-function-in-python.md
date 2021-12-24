# Python 中的 matplotlib . axis . tick . get _ zorder()函数

> 原文:[https://www . geeksforgeeks . org/matplotlib-axis-tick-get _ zorder-python 中的函数/](https://www.geeksforgeeks.org/matplotlib-axis-tick-get_zorder-function-in-python/)

[**Matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。这是一个神奇的 Python 可视化库，用于 2D 数组图，并用于处理更广泛的 SciPy 堆栈。

## matplotlib . axis . tick . get _ zorder()函数

matplotlib 库的轴模块中的 **Tick.get_zorder()函数**用于获取艺术家的 zorder。

> **语法:** Tick.get_zorder(self)
> 
> **参数:**该方法不接受任何参数。
> 
> **返回值:**此方法返回艺术家的 zorder。

以下示例说明 matplotlib . axis . tick . get _ zorder()函数在 matplotlib.axis:
**示例 1:**

## 蟒蛇 3

```py
# Implementation of matplotlib function
from matplotlib.axis import Tick
import numpy as np  
import matplotlib.pyplot as plt  

d = np.arange(16).reshape(4, 4)  
xx, yy = np.meshgrid(np.arange(5), np.arange(5))  

fig, ax = plt.subplots()  

ax.set_aspect(1)  
ax.pcolormesh(xx, yy, d)  

ax.text(1.4, 3.5, "Zorder Value : "
        + str(Tick.get_zorder(ax)),  
        fontweight ="bold")

fig.suptitle('matplotlib.axis.Tick.get_zorder() \
function Example', fontweight ="bold")  

plt.show() 
```

**输出:**

![](img/1d7f0a87a1d33a6c06778c4f14a3010f.png)

**例 2:**

## 蟒蛇 3

```py
# Implementation of matplotlib function
from matplotlib.axis import Tick
import numpy as np  
import matplotlib.pyplot as plt  

xx = np.random.rand(3, 4)  

fig, ax = plt.subplots()  

ax.pcolor(xx)  
ax.set_zorder(3)  

ax.set_title( "Zorder Value : "
        + str(Tick.get_zorder(ax)),  
        fontweight ="bold")  

fig.suptitle('matplotlib.axis.Tick.get_zorder() \
function Example', fontweight ="bold")  

plt.show() 
```

**输出:**

![](img/5f06a31d95152a5b9ecbdf74ec29744d.png)
# Python 中的 matplotlib . axis . axis . set _ zorder()函数

> 原文:[https://www . geesforgeks . org/matplotlib-axis-axis-set _ zorder-python 中的函数/](https://www.geeksforgeeks.org/matplotlib-axis-axis-set_zorder-function-in-python/)

[**Matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。这是一个神奇的 Python 可视化库，用于 2D 数组图，并用于处理更广泛的 SciPy 堆栈。

## matplotlib . axis . axis . set _ zorder()函数

matplotlib 库的 Axis 模块中的 **Axis.set_zorder()函数**用于为艺术家设置 zorder。

> **语法:** Axis.set_zorder(self，level)
> 
> **参数:**该方法接受以下参数。
> 
> *   **级别:**该参数包含浮点值。
> 
> **返回值:**此方法不返回值。

下面的例子说明了 matplotlib.axis . axis . set _ zorder()函数在 matplotlib . axis 中的作用:

**例 1:**

## 蟒蛇 3

```py
# Implementation of matplotlib function
from matplotlib.axis import Axis
import numpy as np  
import matplotlib.pyplot as plt  

d = np.arange(25).reshape(5, 5)  
xx, yy = np.meshgrid(np.arange(6), np.arange(6))  

fig, ax = plt.subplots()  

ax.set_aspect(1)  
m = ax.pcolormesh(xx**2, yy**2, d**2) 

Axis.set_zorder(m, -10) 

plt.title('matplotlib.axis.Axis.set_zorder() \
function Example\n', fontweight ="bold")  

plt.show() 
```

**输出:**

![](img/38c3d1e9a7bc8b21f07132a869ac9fb2.png)

**例 2:**

## 蟒蛇 3

```py
# Implementation of matplotlib function
from matplotlib.axis import Axis
import numpy as np  
import matplotlib.pyplot as plt  

xx = np.random.rand(6, 5)  

fig, (ax3, ax4) = plt.subplots(1, 2)  

m = ax3.pcolor(xx)  

ax3.set_title("No Zorder value ")  

m = ax4.pcolor(xx)  
Axis.set_zorder(m, -7)  

ax4.set_title("Zorder Value : -7")

fig.suptitle('matplotlib.axis.Axis.set_zorder() \
function Example\n', fontweight ="bold")  

plt.show() 
```

**输出:**

![](img/5a43064fbfdfccf1b6bd771a1d9c14e3.png)
# Python 中的 matplotlib . axis . axis . set _ visible()函数

> 原文:[https://www . geesforgeks . org/matplotlib-axis-axis-set _ visible-python 中的函数/](https://www.geeksforgeeks.org/matplotlib-axis-axis-set_visible-function-in-python/)

[**Matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。这是一个神奇的 Python 可视化库，用于 2D 数组图，并用于处理更广泛的 SciPy 堆栈。

## matplotlib . axis . axis . set _ visible()函数

matplotlib 库的 Axis 模块中的 **Axis.set_visible()函数**用于设置艺术家的可见性。

> **语法:** Axis.set_visible(self，b)
> 
> **参数:**该方法接受以下参数。
> 
> *   **b:** 该参数为布尔值。
> 
> **返回值:**此方法不返回值。

下面的例子说明了 matplotlib . axis . axis . set _ visible()函数在 matplotlib.axis:

**例 1:**

## 蟒蛇 3

```
# Implementation of matplotlib function
from matplotlib.axis import Axis
import matplotlib.pyplot as plt  
from mpl_toolkits.axisartist.axislines import Subplot  

fig = plt.figure()  

ax = Subplot(fig, 111)  
fig.add_subplot(ax)  

Axis.set_visible(ax.axis["right"], False)  
Axis.set_visible(ax.axis["top"], False)

fig.suptitle('matplotlib.axis.Axis.set_visible() \
function Example\n', fontweight ="bold")  

plt.show() 
```

**输出:**

![](img/8c50109e6a905f80a9f0ef0621ea0b45.png)

**例 2:**

## 蟒蛇 3

```
# Implementation of matplotlib function
from matplotlib.axis import Axis
import matplotlib.pyplot as plt  
import numpy as np 

X = np.arange(-20, 20, 0.5)  
Y = np.arange(-20, 20, 0.5)  
U, V = np.meshgrid(X, Y)  

fig, ax = plt.subplots()  
ax.quiver(X, Y, U, V)  
w = ax.get_xaxis() 

Axis.set_visible(w, False) 

fig.suptitle('matplotlib.axis.Axis.set_visible() \
function Example\n', fontweight ="bold")  

plt.show() 
```

**输出:**

![](img/9d41238e10dcd77e3af0d8e51a5c2060.png)
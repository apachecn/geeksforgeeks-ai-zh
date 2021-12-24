# Python 中的 matplotlib . axis . axis . get _ window _ extent()函数

> 原文:[https://www . geeksforgeeks . org/matplotlib-axis-axis-get _ window _ extend-python 中的函数/](https://www.geeksforgeeks.org/matplotlib-axis-axis-get_window_extent-function-in-python/)

[**Matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。这是一个神奇的 Python 可视化库，用于 2D 数组图，并用于处理更广泛的 SciPy 堆栈。

## matplotlib . axis . axis . get _ window _ extent()函数

matplotlib 库的 Axis 模块中的 **Axis.get_window_extent()函数**用于获取显示空间中的坐标轴包围盒。

> **语法:** Axis.get_window_extent(self，渲染器)
> 
> **参数:**该方法接受以下参数。
> 
> *   **渲染器:**这个参数是 RendererBase 子类。
> 
> **返回值:**该方法返回显示空间中的轴边界框。

以下示例说明了 matplotlib . axis . get _ window _ extent()函数在 matplotlib.axis:
**示例 1:**

## 蟒蛇 3

```py
# Implementation of matplotlib function
from matplotlib.axis import Axis
import numpy as np 
import matplotlib.pyplot as plt 

X = np.arange(-10, 10, 1.5) 
Y = np.arange(-10, 10, 1.5) 
U, V = np.meshgrid(X, Y) 

fig, ax = plt.subplots() 

ax.quiver(X, Y, U, V) 

fig.canvas.draw()   
renderer = fig.canvas.renderer 

# use of get_window_extent() method 
val = Axis.get_window_extent(ax, renderer) 
print("Value Return by get_window_extent():") 
print(val)    

fig.suptitle('matplotlib.axis.Axis.get_window_extent() \
function Example\n', fontweight ="bold")  

plt.show() 
```

**输出:**

![](img/d41a99fc2c48e349def1556de2af7c59.png)

```py
Value Return by get_window_extent():
Bbox(x0=0.0, y0=0.0, x1=0.0, y1=0.0)

```

**例 2:**

## 蟒蛇 3

```py
# Implementation of matplotlib function
from matplotlib.axis import Axis
import matplotlib.pyplot as plt 
import numpy as np   

xx = np.random.rand(10, 10) 

fig, ax = plt.subplots() 

m = ax.pcolor(xx) 
m.set_zorder(-20) 

fig.canvas.draw()   
renderer = fig.canvas.renderer 

# use of get_window_extent() method 
val = Axis.get_window_extent(ax, renderer) 
print("Value Return by get_window_extent():") 
print(val) 

fig.suptitle('matplotlib.axis.Axis.get_window_extent() \
function Example\n', fontweight ="bold")  

plt.show() 
```

**输出:**

![](img/9cb9825a26ad896d36bbe4e011a89168.png)

```py
Value Return by get_window_extent():
Bbox(x0=0.0, y0=0.0, x1=0.0, y1=0.0)

```
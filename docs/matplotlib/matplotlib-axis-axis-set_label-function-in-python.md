# Python 中的 Matplotlib.axis.Axis.set_label()函数

> 原文:[https://www . geesforgeks . org/matplotlib-axis-axis-set _ label-function-in-python/](https://www.geeksforgeeks.org/matplotlib-axis-axis-set_label-function-in-python/)

[**Matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。这是一个神奇的 Python 可视化库，用于 2D 数组图，并用于处理更广泛的 SciPy 堆栈。

## Matplotlib.axis.Axis.set_label()函数

matplotlib 库的 Axis 模块中的 **Axis.set_label()函数**用于设置将在图例中显示的标签。

> **语法:** Axis.set_label(self，s)
> 
> **参数:**该方法接受以下参数。
> 
> *   **s:** 此参数通过调用 str 转换为字符串。
> 
> **返回值:**此方法返回艺术家的采摘行为。

下面的例子说明了 matplotlib.axis.Axis.set_label()函数在 matplotlib.axis 中的作用:

**例 1:**

## 蟒蛇 3

```
# Implementation of matplotlib function
from matplotlib.axis import Axis
import matplotlib.pyplot as plt  
import numpy as np  
from matplotlib.collections import EllipseCollection  

x = np.arange(5)  
y = np.arange(7)  
X, Y = np.meshgrid(x**2, y**3)  

XY = np.column_stack((X.ravel(), Y.ravel()))  

fig, ax = plt.subplots()  

ec = EllipseCollection(5, 7, 5, units ='y',  
                       offsets = XY * 0.5,  
                       transOffset = ax.transData,  
                       cmap ="plasma")  

ec.set_array((X * Y + X * X).ravel())  

ax.add_collection(ec)  
ax.autoscale_view()  

ax.set_xlabel('X')  
ax.set_ylabel('y')  

cbar = plt.colorbar(ec)  
cbar.set_label('X + Y')    

fig.suptitle('matplotlib.axis.Axis.set_label() \
function Example\n', fontweight ="bold")  

plt.show() 
```

**输出:**

![](img/4b4fe1b8a2db1c7317934297e87c2520.png)

**例 2:**

## 蟒蛇 3

```
# Implementation of matplotlib function
from matplotlib.axis import Axis
import matplotlib.pyplot as plt  
import numpy as np  

np.random.seed(19680801)  

n = 100000
x = np.random.standard_normal(n)  
y = 2 * np.random.standard_normal(n)  
z =[1, 2, 3, 4]  

fig, ax = plt.subplots()  
hb = ax.hexbin(x, y, 
               gridsize = 50, 
               bins ='log', 
               cmap ='bone')    

cb = fig.colorbar(hb, ax = ax)  
cb.set_label('log')    

fig.suptitle('matplotlib.axis.Axis.set_label() \
function Example\n', fontweight ="bold")  

plt.show() 
```

**输出:**

![](img/fa4eced468fba80df4a8eb9b1a074c2a.png)
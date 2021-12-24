# Python 中的 Matplotlib.axis.Tick.set()函数

> 原文:[https://www . geeksforgeeks . org/matplotlib-axis-tick-set-function-in-python/](https://www.geeksforgeeks.org/matplotlib-axis-tick-set-function-in-python/)

[**Matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。这是一个神奇的 Python 可视化库，用于 2D 数组图，并用于处理更广泛的 SciPy 堆栈。

## matplotlib.axis.Tick.set()函数

matplotlib 库轴模块中的 **Tick.set()函数**是一个属性批量设置器。传递 kwargs 以设置属性。

> **语法:** Tick.set(self，**kwargs)
> 
> **参数:**此方法不接受除**kwargs 以外的任何参数。
> 
> **返回值:**此方法不返回值。

以下示例说明 matplotlib.axis.Tick.set()函数在 matplotlib.axis:
**示例 1:**

## 蟒蛇 3

```
# Implementation of matplotlib function
from matplotlib.axis import Tick
import matplotlib  
import matplotlib.pyplot as plt  
import numpy as np  

t = np.arange(0.0, 2, 0.001)  
s = 1 + np.sin(4 * np.pi * t)*0.2

fig, ax = plt.subplots()  
ax.plot(t, s)  

Tick.set(ax, xlabel ='X-Axis', ylabel ='Y-Axis',  
    xlim =(0, 1.5), ylim =(0.5, 1.5))  

ax.grid()  

fig.suptitle('matplotlib.axis.Tick.set() \
function Example', fontweight ="bold")  

plt.show() 
```

**输出:**

![](img/35fa3583607c1b088622788ddfde8737.png)

**例 2:**

## 蟒蛇 3

```
# Implementation of matplotlib function
from matplotlib.axis import Tick
import numpy as np  
import matplotlib.pyplot as plt  
np.random.seed(19680801)  

fig, ax = plt.subplots()  

x, y, s, c = np.random.rand(4, 100)  
s *= 10000

ax.scatter(x**2, y**2, s, c**2) 

Tick.set(ax, xlabel ='X-Axis', ylabel ='Y-Axis',  
   xlim =(0, 0.5), ylim =(0, 0.5))  

fig.suptitle('matplotlib.axis.Tick.set() \
function Example', fontweight ="bold")  

plt.show() 
```

**输出:**

![](img/f98a719267f443c8c9f5b297fcdc9fbb.png)
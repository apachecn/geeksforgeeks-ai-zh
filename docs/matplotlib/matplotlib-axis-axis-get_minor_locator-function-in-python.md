# Python 中的 matplotlib . axis . axis . get _ minor _ locator()函数

> 原文:[https://www . geeksforgeeks . org/matplotlib-axis-axis-get _ minor _ locator-python 中的函数/](https://www.geeksforgeeks.org/matplotlib-axis-axis-get_minor_locator-function-in-python/)

[**Matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。这是一个神奇的 Python 可视化库，用于 2D 数组图，并用于处理更广泛的 SciPy 堆栈。

## matplotlib . axis . axis . get _ minor _ locator()函数

matplotlib 库的 Axis 模块中的 **Axis.get_minor_locator()函数**用于获取 minor ticker 的定位器。

> **语法:** Axis.get_minor_locator(自身)
> 
> **参数:**该方法不接受任何参数。
> 
> **返回值:**此方法返回次要跑马灯的定位器。

以下示例说明 matplotlib . axis . axis . get _ minor _ locator()函数在 matplotlib.axis:
**示例 1:**

## 蟒蛇 3

```py
# Implementation of matplotlib function 
import numpy as np
from matplotlib.axis import Axis  
import matplotlib.pyplot as plt   

x = np.linspace(0, 10, 1000) 
y = np.sin(2 * x) 

fig = plt.figure() 
ax = fig.add_subplot(111) 

ax.plot(x, y)
ax.grid()

print(Axis.get_minor_locator(ax.yaxis))

plt.title("Matplotlib.axis.Axis.get_minor_locator()\n\
Function Example", fontsize = 12, fontweight ='bold') 
plt.show()
```

**输出:**

![](img/a3bc87fbf005ac3cc4c23a5ab8ea1768.png)

```py
<matplotlib.ticker.NullLocator object at 0x086D8C30>

```

**例 2:**

## 蟒蛇 3

```py
# Implementation of matplotlib function 
import numpy as np
from matplotlib.axis import Axis  
import matplotlib.pyplot as plt   

np.random.seed(19680801)  

fig, ax = plt.subplots()  

x, y, s, c = np.random.rand(4, 100)  
s *= 100

ax.scatter(x, y, s, c)
ax.grid()  

print(Axis.get_minor_locator(ax.xaxis))

plt.title("Matplotlib.axis.Axis.get_minor_locator()\n\
Function Example", fontsize = 12, fontweight ='bold') 
plt.show()
```

**输出:**

![](img/1e11205046a008990f12451e7ecc547f.png)

```py
<matplotlib.ticker.NullLocator object at 0x08AE9830>

```
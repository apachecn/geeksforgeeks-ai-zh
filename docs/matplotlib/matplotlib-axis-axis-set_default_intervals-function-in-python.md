# Python 中的 matplotlib . axis . axis . set _ default _ intervals()函数

> 原文:[https://www . geesforgeks . org/matplotlib-axis-axis-set _ default _ intervals-python 中的函数/](https://www.geeksforgeeks.org/matplotlib-axis-axis-set_default_intervals-function-in-python/)

[**Matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。这是一个神奇的 Python 可视化库，用于 2D 数组图，并用于处理更广泛的 SciPy 堆栈。

## matplotlib . axis . axis . set _ default _ intervals()函数

matplotlib 库的 Axis 模块中的 **Axis.set_default_intervals()函数**用于设置轴数据和视图间隔的默认限制。

> **语法:**axis . set _ default _ intervals(self)
> 
> **参数:**该方法不接受任何参数。
> 
> **返回值:**此方法不返回值。

下面的例子说明了 matplotlib.axis . axis . set _ default _ intervals()函数在 matplotlib . axis 中的作用:

**例 1:**

## 蟒蛇 3

```
# Implementation of matplotlib function
from matplotlib.axis import Axis
import matplotlib.pyplot as plt
import numpy as np 

fig = plt.figure()

x = np.linspace(0,4*np.pi,100)
y = 2*np.sin(x)

ax = fig.add_subplot()
ax.plot(x,y)

ax.xaxis.set_default_intervals()

ax.grid() 

fig.suptitle("""matplotlib.axis.Axis.set_default_intervals()
function Example\n""", fontweight ="bold")  

plt.show()
```

**输出:**

![](img/97a16612073f2727efb539d4466e7f08.png)

**例 2:**

## 蟒蛇 3

```
# Implementation of matplotlib function
from matplotlib.axis import Axis
import matplotlib.pyplot as plt
import numpy as np 

np.random.seed(10**7)  
geeks = np.random.randn(40)  

fig, ax = plt.subplots()  
ax.acorr(geeks, usevlines = True,  
         normed = True, maxlags = 9,lw = 3)  

ax.grid(True)

ax.xaxis.set_default_intervals()

fig.suptitle("""matplotlib.axis.Axis.set_default_intervals()
function Example\n""", fontweight ="bold")  

plt.show()
```

**输出:**

![](img/af4610c1a1d2b81b3a2e1663162fc6ad.png)
# Python 中的 matplotlib . axes . axes . get _ agg _ filter()

> 原文:[https://www . geeksforgeeks . org/matplotlib-axes-axes-get _ agg _ filter-in-python/](https://www.geeksforgeeks.org/matplotlib-axes-axes-get_agg_filter-in-python/)

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**轴类**包含了大部分的图形元素:轴、刻度、线二维、文本、多边形等。，并设置坐标系。Axes 的实例通过回调属性支持回调。

## matplotlib . axes . axes . get _ agg _ filter()函数

matplotlib 库的 Axes 模块中的 **Axes.get_agg_filter()函数**用于获取用于 agg 过滤的过滤函数。

> **语法:** Axes.get_agg_filter(self)
> 
> **参数:**该方法不接受任何参数。
> 
> **返回:**该方法返回用于 agg 过滤的过滤函数。

下面的例子说明了 matplotlib.axes . axes . get _ agg _ filter()函数在 matplotlib . axes 中的作用:

**例 1:**

```py
# Implementation of matplotlib function 
import numpy as np 
import matplotlib.pyplot as plt 

xx = np.random.rand(16, 30) 

fig, ax = plt.subplots() 

m = ax.pcolor(xx) 
m.set_zorder(-20)

w = ax.get_agg_filter()
ax.set_title("Value Return by get_agg_filter(): "+ str(w))

fig.suptitle('matplotlib.axes.Axes.get_agg_filter() \
function Example', fontweight ="bold") 

plt.show() 
```

**输出:**
![](img/7d43c7e57b4c19726467541031d4afde.png)

**例 2:**

```py
# Implementation of matplotlib function
import matplotlib.pyplot as plt
import numpy as np

np.random.seed(10**7)
geeks = np.random.randn(100)

fig, ax = plt.subplots()
ax.acorr(geeks, usevlines = True, normed = True, 
         maxlags = 80, lw = 3)

ax.grid(True)

w = ax.get_agg_filter()
ax.set_title("Value Return by get_agg_filter(): "+ str(w))

fig.suptitle('matplotlib.axes.Axes.get_agg_filter()\
 function Example', fontweight ="bold") 

plt.show() 
```

**输出:**
![](img/6dbfc1f210081c3b75821571216acf39.png)
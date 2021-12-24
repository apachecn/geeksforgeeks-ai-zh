# matplotlib . axes . get _ ylabel()用 Python

表示

> 哎哎哎:# t0]https://www . geeksforgeeks . org/matplotlib-axes-get _ ylabel-in-python/

**[Matplotlib](https://www.geeksforgeeks.org/python-introduction-matplotlib/)** 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。**轴类**包含了大部分的图形元素:轴、刻度、线二维、文本、多边形等。，并设置坐标系。Axes 的实例通过回调属性支持回调。

## matplot lib . axes . axes . get _ ylabel()函数

matplotlib 库的 Axes 模块中的 **Axes.get_ylabel()函数**用于获取 ylabel 文本字符串。

> **语法:** Axes.get_ylabel(self)
> 
> **参数:**该方法不接受任何参数。
> 
> **返回:**该函数返回依拉贝尔文本字符串。

下面的例子说明了 matplotlib.axes . axes . get _ ylabel()函数在 matplotlib . axes 中的作用:

**例 1:**

```py
import matplotlib.pyplot as plt
import numpy as np

t = np.arange(0.01, 5.0, 0.01)
s = np.exp(-t)

fig, ax = plt.subplots()

ax.plot(t, s)
ax.set_ylim(1, 0)
ax.set_ylabel('Display Y-axis Label', fontweight ='bold')
ax.grid(True)

w = ax.get_ylabel()
ax.set_ylabel("")
ax.text(1.5, 0.58, "Previously assigned Y-Label : \n\n"+str(w),
       fontsize = 12)
fig.suptitle("matplotlib.axes.Axes.get_ylabel() function\
 Example\n", fontweight ="bold")
plt.show()
```

**输出:**
![](img/bee082c170e2429f05c8576acae58aa2.png)

**例 2:**

```py
# Implementation of matplotlib function
import numpy as np
import matplotlib.pyplot as plt
import matplotlib.cbook as cbook

with cbook.get_sample_data('goog.npz') as datafile:
    price_data = np.load(datafile)['price_data'].view(np.recarray)
price_data = price_data[-250:]  # get the most recent 250 trading days

delta1 = np.diff(price_data.adj_close) / price_data.adj_close[:-1]

volume = (25 * price_data.volume[:-2] / price_data.volume[0])**(2.2)
close = (0.03 * price_data.close[:-2] / 0.03 * price_data.open[:-2])**2

fig, ax = plt.subplots()
ax.scatter(delta1[:-1], delta1[1:], 
           c = close, s = volume, 
           alpha = 0.5)

ax.set_ylabel(r'Y-axis contains $\Delta_{i + 1}$ values',
              fontweight ='bold')
ax.grid(True)

w = ax.get_ylabel()
ax.set_ylabel("")
ax.set_xlabel(w)
ax.text(-0.1, 0.1, "Previously assigned Y-Label is now Assigned\
to X-Label", fontsize = 12, fontweight ="bold")

fig.suptitle("matplotlib.axes.Axes.get_ylabel() function \
Example\n", fontweight ="bold")
plt.show()
```

**输出:**
![](img/ede0a2a50751cf035befb823bb4453e7.png)
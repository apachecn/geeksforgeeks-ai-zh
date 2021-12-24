# Python 中的 matplotlib . axis . axis . get _ label _ position()函数

> 原文:[https://www . geeksforgeeks . org/matplotlib-axis-axis-get _ label _ position-function-in-python/](https://www.geeksforgeeks.org/matplotlib-axis-axis-get_label_position-function-in-python/)

[**Matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。这是一个神奇的 Python 可视化库，用于 2D 数组图，并用于处理更广泛的 SciPy 堆栈。

## matplotlib . axis . axis . get _ label _ position()函数

matplotlib 库的 Axis 模块中的 **Axis.get_label_position()函数**用于获取标签位置。

> **语法:**axis . get _ label _ position(self)
> 
> **参数:**该方法不接受任何参数。
> 
> **返回值:**此方法返回标签位置。

下面的例子说明了 matplotlib.axis . axis . get _ label _ position()函数在 matplotlib . axis 中的作用:

**例 1:**

## 蟒蛇 3

```py
# Implementation of matplotlib function 
from matplotlib.axis import Axis
import numpy as np
import matplotlib.pyplot as plt

fig, ax2 = plt.subplots(sharex = True)
fig.subplots_adjust(left=0.2, wspace=0.6)
box = dict(facecolor='green', pad=5, alpha=0.2)

ax2.plot(20*np.random.rand(10))
ax2.xaxis.set_label_text('X - Label', bbox=box)
ax2.set_xlim(0, 10)
print("Position of Label :",ax2.xaxis.get_label_position())

fig.suptitle("Matplotlib.axis.Axis.get_label_position()\
Function Example", fontsize = 12, fontweight ='bold') 

plt.show()
```

**输出:**

![](img/eb7f7e6f244ff36844781d8a33416ffe.png)

```py
Position of Label : bottom

```

**例 2:**

## 蟒蛇 3

```py
# Implementation of matplotlib function 
from matplotlib.axis import Axis
import numpy as np
import matplotlib.pyplot as plt

fig, (ax1, ax2) = plt.subplots(2, 1, sharex = True)
fig.subplots_adjust(left=0.2, wspace=0.6)
box = dict(facecolor='green', pad=5, alpha=0.2)

np.random.seed(19680801)
ax1.plot(2*np.random.rand(10))
ax1.set_title('Label is not aligned')
ax1.yaxis.set_label_text('Default', bbox=box)
ax1.set_ylim(0, 20)
print("Position of Label in Axes 1 :",
      ax1.yaxis.get_label_position())

ax2.set_title('\nLabel is aligned')
ax2.plot(20*np.random.rand(10))
ax2.yaxis.set_label_text('Adjusted', bbox=box)
ax2.yaxis.set_label_position('right')
ax2.set_ylim(0, 20)
print("Position of Label in Axes 2 :",
      ax2.yaxis.get_label_position())

fig.suptitle("Matplotlib.axis.Axis.get_label_position()\
Function Example", fontsize = 12, fontweight ='bold')

plt.show()
```

**输出:**

![](img/cacebdd15a1fa92f173b93566d02438d.png)

```py
Position of Label in Axes 1 : left
Position of Label in Axes 2 : right

```
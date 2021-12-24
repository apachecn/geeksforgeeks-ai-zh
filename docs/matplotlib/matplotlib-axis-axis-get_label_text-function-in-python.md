# Python 中的 matplotlib . axis . axis . get _ label _ text()函数

> 原文:[https://www . geeksforgeeks . org/matplotlib-axis-axis-get _ label _ text-function-in-python/](https://www.geeksforgeeks.org/matplotlib-axis-axis-get_label_text-function-in-python/)

[**Matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是 Python 中的一个库，是 NumPy 库的数值-数学扩展。这是一个神奇的 Python 可视化库，用于 2D 数组图，并用于处理更广泛的 SciPy 堆栈。

## matplotlib . axis . axis . get _ label _ text()函数

matplotlib 库的 Axis 模块中的 **Axis.get_label_text()函数**用于获取标签的文本。

> **语法:** Axis.get_label_text(self)
> 
> **参数:**该方法不接受任何参数。
> 
> **返回值:**该方法返回标签的文本。

下面的例子说明了 matplotlib.axis . axis . get _ label _ text()函数在 matplotlib . axis 中的作用:

**例 1:**

## 蟒蛇 3

```
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
print("Text of the Label :",ax2.xaxis.get_label_text())

fig.suptitle("Matplotlib.axis.Axis.get_label_text()\
Function Example", fontsize = 12, fontweight ='bold') 

plt.show()
```

**输出:**

![](img/1f00b06ec03049c679b5bcef97c37e77.png)

```
Text of the Label : X - Label

```

**例 2:**

## 蟒蛇 3

```
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
print("Text of Label in Axes 1 :",ax1.yaxis.get_label_text())

ax2.set_title('\nLabel is aligned')
ax2.plot(20*np.random.rand(10))
ax2.yaxis.set_label_text('Adjusted', bbox=box)
ax2.yaxis.set_label_position('right')
ax2.set_ylim(0, 20)
print("Text of Label in Axes 2 :",ax2.yaxis.get_label_text())

fig.suptitle("Matplotlib.axis.Axis.get_label_text()\
Function Example", fontsize = 12, fontweight ='bold') 

plt.show()
```

**输出:**

![](img/86963ec0f66487299b890f10891c40b2.png)

```
Text of Label in Axes 1 : Default
Text of Label in Axes 2 : Adjusted

```
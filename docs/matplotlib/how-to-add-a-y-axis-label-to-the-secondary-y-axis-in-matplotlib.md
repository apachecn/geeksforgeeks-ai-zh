# 如何在 Matplotlib 中给副 Y 轴添加 Y 轴标签？

> 原文:[https://www . geeksforgeeks . org/如何将 y 轴标签添加到 matplotlib 中的次级 y 轴/](https://www.geeksforgeeks.org/how-to-add-a-y-axis-label-to-the-secondary-y-axis-in-matplotlib/)

有时，在通过图表分析任何数据时，我们需要两个 x 轴或 y 轴来深入了解数据。[Python 的 Matplotlib 库](https://www.geeksforgeeks.org/python-introduction-matplotlib/)是目前最流行的数据可视化库，我们可以在 Matplotlib 中生成任何类型的图。我们可以创建一个具有两个 y 轴的图，并且可以为两个 y 轴提供不同的标签。借助 [twinx()](https://www.geeksforgeeks.org/matplotlib-axes-axes-twinx-in-python/) 功能，我们可以通过创建或使用两个不同轴的对象来绘制两个不同 y 轴的图。首先，我们创建图形和轴对象，并制作第一个图。我们还在创建的轴对象的帮助下设置了 x 轴和 y 轴标签。

**轴对象:** [轴](https://www.geeksforgeeks.org/matplotlib-axes-class/)是创建支线剧情最基本最灵活的单位。轴用于在图形中的任何位置放置地块。一个给定的图形可以包含许多轴，但是一个给定的轴对象只能在一个图形中。

### **进场:**

*   导入包。
*   使用 axes 对象并创建一个子图。
*   使用 twinx()定义绘图值。
*   现在标记轴。
*   展示剧情。

**例 1:**

在本例中，借助 twinx()函数，我们使用两个不同的轴对象 a 和 a2 创建了一个具有两个不同 y 轴的绘图。ax.twinx()为与原始 y 轴相反的 y 轴创建一个新的 axis 对象 ax2。第二个 axes 对象 ax2 用于绘制第二个 y 轴变量并更新其标签。

## 蟒蛇 3

```py
# Adding a Y-Axis Label to the Secondary Y-Axis in Matplotlib
# importing the libraries
import numpy as np
import matplotlib.pyplot as plt

# creating data for plot
# data arrangement between 0 and 50
# with the difference of 2
# x-axis
x = np.arange(0, 50, 2)

# y-axis values
y1 = x**2

# secondary y-axis values
y2 = x**3

# plotting figures by creating aexs object
# using subplots() function
fig, ax = plt.subplots(figsize = (10, 5))
plt.title('Example of Two Y labels')

# using the twinx() for creating another
# axes object for secondary y-Axis
ax2 = ax.twinx()
ax.plot(x, y1, color = 'g')
ax2.plot(x, y2, color = 'b')

# giving labels to the axises
ax.set_xlabel('x-axis', color = 'r')
ax.set_ylabel('y1-axis', color = 'g')

# secondary y-axis label
ax2.set_ylabel('Secondary y-axis', color = 'b')

# defining display layout
plt.tight_layout()

# show plot
plt.show()
```

**输出:**

![](img/ad09e6fded65f3ea79a7f0817d539248.png)

**例 2:**

在本例中，我们使用相同的方法创建了条形图。

## 蟒蛇 3

```py
# Adding a Y-Axis Label to the
# Secondary Y-Axis in Matplotlib
# importing the libraries
import numpy as np
import matplotlib.pyplot as plt

# creating data for plot
# data arrangement between 0 and 50 with the difference of 2
# x-axis values
x = np.arange(0, 50, 2)

#y-axis values
y1 = x**2

# secondary y-axis values
y2 = x**3

# plotting figures by creating aexs object
# using subplots() function
fig, ax = plt.subplots(figsize = (10, 5))
plt.title('Example of Two Y labels')

# using the twinx() for creating
# another axes object for secondary y-Axis
ax2 = ax.twinx()
# creating a bar plot
ax.bar(x, y1, color = 'g')
ax2.bar(x, y2, color = 'b')

# giving labels to the axises
ax.set_xlabel('x-axis', color = 'r')
ax.set_ylabel('y1-axis', color = 'g')

# secondary y-axis label
ax2.set_ylabel('Secondary y-axis', color = 'b')

# defining display layout
plt.tight_layout()

# show plot
plt.show()
```
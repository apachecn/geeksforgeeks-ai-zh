# 使用 Matplotlib

在 Python 中的两条曲线之间制作填充多边形

> 原文:[https://www . geesforgeks . org/make-filled-polygons-two-in-python-use-matplotlib/](https://www.geeksforgeeks.org/make-filled-polygons-between-two-curves-in-python-using-matplotlib/)

**Matplotlib** 是 Python 中一个惊人的可视化库，用于数组的 2D 图。 [Matplotlib](http://geeksforgeeks.org/python-matplotlib-an-overview/) 是一个基于 NumPy 数组构建的多平台数据可视化库，旨在与更广泛的 SciPy 堆栈协同工作。
要在两条曲线之间创建填充多边形，需要在 y1 和 y2 之间创建多边形集合填充。
**上述任务的参数:**

1.  **x:** 是长度为 N 的数组，保存 x 的数据。

2.  **y1:** 它是长度为 N 的数组或标量，保存 y 的数据

3.  **y2:** 是长度为 N 的数组或标量，保存 y 的数据

**例:**

## 蟒蛇 3

```
import matplotlib.pyplot as plt
import numpy as np
# set the width
width = 3.5

# set the height
height = 2.5

# set the depth
depth = 65

# plot the figure
plt.figure(figsize =(width, height), dpi = depth)

# set the x array of length 3
x = [1, 3, 6]

# set y1 array of length 3
y1 = [2, 3.5, 4]

# set y2 array of length 3
y2 = [3, 4, 5.5]

# fill the horizontal area between y1 and y2
plt.fill_between(x, y1, y2)

# show the plotted figure
plt.show()
```
# Matplotlib–Python 中的折线图

> 原文:[https://www . geesforgeks . org/line-chart-in-matplotlib-python/](https://www.geeksforgeeks.org/line-chart-in-matplotlib-python/)

**Matplotlib** 是 Python 中的数据可视化库。matplotlib 的子库 [**pyplot**](https://www.geeksforgeeks.org/pyplot-in-matplotlib/) 是帮助创建各种图表的功能集合。 ***折线图*** 用于表示不同轴上两个数据 X 和 Y 之间的关系。在这里，我们将看到 Python 中折线图的一些示例:

## 简单线图

首先导入 Matplotlib.pyplot 库，用于绘制函数。此外，根据要求导入 Numpy 库。然后定义数据值 x 和 y .

## python 3

```
# importing the required libraries
import matplotlib.pyplot as plt
import numpy as np

# define data values
x = np.array([1, 2, 3, 4])  # X-axis points
y = x*2  # Y-axis points

plt.plot(x, y)  # Plot the chart
plt.show()  # display
```
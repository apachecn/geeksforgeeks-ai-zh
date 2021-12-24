# 如何在 Matplotlib 中改变轴标签的大小？

> 原文:[https://www . geeksforgeeks . org/如何更改 matplotlib 中轴标签的大小/](https://www.geeksforgeeks.org/how-to-change-the-size-of-axis-labels-in-matplotlib/)

**Matplotlib** 是一个很棒的数据绘图工具。它用于可视化数据，也用于在演示中向您的团队展示数据，或者供您自己将来参考。因此，在展示时，可能会出现“X 标签”和“y 标签”不可见的情况，因此，我们可能需要更改其字体大小。因此，在本文中，我们将了解如何在 Matplotlib 中更改轴标签的大小。

**开始之前我们先用 matplotlib 画一个简单的图。**

## 蟒蛇 3

```
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [9, 8, 7, 6, 5]

fig, ax = plt.subplots()
ax.plot(x, y)

ax.set_xlabel('x-axis')
ax.set_ylabel('y-axis')

plt.show()
```
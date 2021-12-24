# 在 Matplotlib 中的直方图条之间添加间隔

> 原文:[https://www . geeksforgeeks . org/add-matplotlib 中柱状图条间距/](https://www.geeksforgeeks.org/add-space-between-histogram-bars-in-matplotlib/)

Matplotlib 是 python 编程语言中的绘图库，默认情况下，它是 Python 语言中 NumPy 库的数字数学扩展。在用 python 语言编程时，我们使用 matplotlib 库包进行图形和直方图可视化。但是在 python 中使用 matplotlib 绘制直方图时，它缺少相邻条之间的分割或间隔。这使得直方图的处理变得非常繁琐，并且变得非常难以解释。在本文中，我们将研究如何在 matplotlib 中的直方图条之间添加空间。
**我们用这个例子来理解:**

**示例 1:** 创建一个简单的图。

## 蟒蛇 3

```py
import matplotlib.pyplot as plt

values = [1, 2, 3, 3, 4, 5, 6, 6, 7, 8]

# Adjust the bar widths here
plt.hist(values)

plt.ylabel("Quantity")
plt.xlabel("Value")
plt.show()
```
# 如何在 Matplotlib 图上手动添加带有颜色框的图例？

> 原文:[https://www . geesforgeks . org/如何手动添加带颜色框的图例-matplotlib-figure/](https://www.geeksforgeeks.org/how-to-manually-add-a-legend-with-a-color-box-on-a-matplotlib-figure/)

图例基本上是图中描述图中元素的区域。Matplotlib 为此提供了一个名为 legend()的内置方法。该方法的语法如下:

**示例:**添加简单传说

## 蟒蛇 3

```
# Import libraries
import matplotlib.pyplot as plt

# Creating plot
plt.plot([1, 2, 3, 4])

plt.title('simple legend example ')

# Creating legend
plt.legend(['simple legend example']) 

# Show plot
plt.show()
```
# 如何在 Matplotlib 中更新一个剧情？

> 原文:[https://www . geesforgeks . org/如何更新 matplotlib 中的绘图/](https://www.geeksforgeeks.org/how-to-update-a-plot-in-matplotlib/)

在本文中，让我们讨论如何在 Matplotlib 中更新一个情节。更新图只意味着绘制数据，然后清除现有的图，然后再次绘制更新的数据，所有这些步骤都在循环中执行。

### 使用的功能:

*   **canvas.draw():** 用于更新已更改的人物。它将重新绘制当前图形。
*   **canvas.flush_events():** 它保存图形用户界面事件，直到用户界面事件处理完毕。这将一直运行到循环结束，并且值将不断更新。

下面是实现。

*   Create data to be drawn using:

## python 3

```
x = np.linspace(0, 10*np.pi, 100)
y = np.sin(x)
```
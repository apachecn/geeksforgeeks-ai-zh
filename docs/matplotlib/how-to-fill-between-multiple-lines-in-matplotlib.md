# Matplotlib 中多行之间如何填充？

> 原文:[https://www . geeksforgeeks . org/matplotlib 中多行之间如何填充/](https://www.geeksforgeeks.org/how-to-fill-between-multiple-lines-in-matplotlib/)

使用 Python 中 Matplotlib 库中的[**fill _ between()**](https://www.geeksforgeeks.org/matplotlib-pyplot-fill_between-in-python/)**函数，我们可以轻松填充 2D 平面上任意多条直线或任意两条水平曲线之间的颜色。**

> *****语法:**matplotlib . pyplot . fill _ between(x，y1，y2=0，其中=无，步长=无，插值=假，*数据=无，* * * kwargs)***

****例 1:** 数学函数的曲线间颜色**f(x)= sin(x)****

**T5

## 蟒 3

T10】

```py
import pylab as plt
import numpy as np

x = np.arange(0.0, 2, 0.01)
y1 = np.sin(2 * np.pi * x)
y2 = 0.8 * np.sin(4 * np.pi * x)

fig, (ax1, ax2, ax3) = plt.subplots(
  3, 1, sharex=True, figsize=(6, 6))

ax1.fill_between(x, y1)
ax1.set_title('fill between y1 and 0')

ax2.fill_between(x, y1, 1)
ax2.set_title('fill between y1 and 1')

ax3.fill_between(x, y1, y2)
ax3.set_title('fill between y1 and y2')
ax3.set_xlabel('x')
fig.tight_layout()
```**
# 如何在 Python 的 Matplotlib 中设置支线剧情之间的间距？

> 原文:[https://www . geeksforgeeks . org/如何设置 python 中 matplotlib 的子情节间距/](https://www.geeksforgeeks.org/how-to-set-the-spacing-between-subplots-in-matplotlib-in-python/)

在本文中，我们将看到如何在 Python 的 Matplotlib 中设置子情节之间的间距。我们来讨论一些概念:

*   [t0 T0】 Matplotlib: Matplotlib is an amazing visual library in Python, which is used for 2D diagrams of arrays. Matplotlib is a multi-platform data visualization library, built on NumPy array and designed to work with a wider SciPy stack. It was launched by john hunter in 2002.
*   **subplots:** The subplots () function in the pyplot module of Matplotlib library is used to create a character and a group of subplots. When we want to show two or more plots in the same picture, we need subplots.

**这里先来看看为什么需要设置空间。**

## 蟒 3

```
# importing packages
import numpy as np
import matplotlib.pyplot as plt

# create data
x=np.array([1, 2, 3, 4, 5])

# making subplots
fig, ax = plt.subplots(2, 2)

# set data with subplots and plot
ax[0, 0].plot(x, x)
ax[0, 1].plot(x, x*2)
ax[1, 0].plot(x, x*x)
ax[1, 1].plot(x, x*x*x)
plt.show()
```
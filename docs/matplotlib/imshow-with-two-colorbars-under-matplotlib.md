# 在 Matplotlib

下用两个颜色条显示

> 原文:[https://www . geesforgeks . org/imshow-with-two-color bar-under-matplotlib/](https://www.geeksforgeeks.org/imshow-with-two-colorbars-under-matplotlib/)

在本文中，我们将学习如何在 Matplotlib 下使用带有两个颜色条的 Imshow。我们来讨论一些概念:

*   [**matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/#:~:text=Matplotlib%20is%20an%20amazing%20visualization,Hunter%20in%20the%20year%202002.) is an amazing visual library in Python, which is used for 2D array diagrams. Matplotlib drawing library is a multi-platform data visualization library based on NumPy array, which aims to work with a wider SciPy stack. It was launched by john hunter in 2002.
*   One of the greatest benefits of visualization is that it allows us to visually access massive amounts of data in a visual way that is easy to digest. Matplotlib consists of several graphs, such as straight line, bar graph, scatter graph, histogram, etc.
*   [**IM SHOW () function**](https://www.geeksforgeeks.org/matplotlib-pyplot-imshow-in-python/) in pyplot module in Matplotlib library is used to display data as images; That is, on a 2D regular grating.
*   [**colorbar () function**](https://www.geeksforgeeks.org/matplotlib-pyplot-colorbar-function-in-python/) in the pyplot module of Matplotlib adds a color bar to the drawing to indicate the color scale.

**一个简单的 Imshow()同一个颜色条**

## python 3

```py
# import libraries
import matplotlib.pyplot as plt
import numpy as np

# create image = 10x10 array
img = np.random.randint(-100, 100, (10, 10))

# make plot
fig, ax = plt.subplots()

# show image
shw = ax.imshow(img)

# make bar
bar = plt.colorbar(shw)

# show plot with labels
plt.xlabel('X Label')
plt.ylabel('Y Label')
bar.set_label('ColorBar')
plt.show()
```
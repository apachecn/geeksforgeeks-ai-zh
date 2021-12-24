# 如何在 Matplotlib 中将传说放置在剧情之外？

> 原文:[https://www . geesforgeks . org/如何放置-图例-matplotlib 中的地块外/](https://www.geeksforgeeks.org/how-to-place-legend-outside-of-the-plot-in-matplotlib/)

在本文中，我们将看到如何在 Matplotlib 中将图例放置在情节之外？我们来讨论一些概念:

*   [t0 T0】 Matplotlib: Matplotlib is an amazing visual library in Python, which is used for 2D diagrams of arrays. Matplotlib is a multi-platform data visualization library, built on NumPy array and designed to work with a wider SciPy stack. It was launched by john hunter in 2002.
*   **Legend:** Legend is an area that describes graphic elements. In matplotlib library, there is a function called legend () for placing legends on axes. The Loc attribute in the legend () is used to specify the location of the legend. The default value of loc is loc= Best (upper left corner).

**在这里，首先我们来看看为什么需要在外面放置图例。**

## 蟒 3

```
# importing packages
import numpy as np
import matplotlib.pyplot as plt

# create data
x=np.linspace(-20, 20, 1000)

# plot the graphs
plt.plot(x,np.sin(x))
plt.plot(x,np.cos(x))

# add legends
plt.legend(["Sine","Cosine"])

plt.show()
```
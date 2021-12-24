# 如何用 Python 中的 Matplotlib 绘制三维立方体？

> 原文:[https://www . geesforgeks . org/how-draw-3d-cube-using-matplotlib-in-python/](https://www.geeksforgeeks.org/how-to-draw-3d-cube-using-matplotlib-in-python/)

在本文中，我们将使用 matplotlib 和 Numpy 处理立方体的 3d 图。立方体是最基本的三维形状之一。立方体是由 6 个相同的正方形面围成的三维实体。立方体有 6 个面，12 个边和 8 个角。所有的面都是同样大小的正方形。立方体的总表面积是 6 个相同正方形的面积之和。

Matplotlib 有各种各样的情节。图表有助于理解趋势，模式，以建立相关性。Matplotlib 是为二维绘图而引入的。3d 绘图是通过导入 mplot3d 工具包实现的。，它附带了您的标准 Matplotlib。导入后，可以通过将关键字 projection =“3D”传递给 Matplotlib 中的任何常规轴创建函数来创建 3D 地块。

### 需要的模块

*   **Matplotlib:** 这是一个 Python 编程的绘图库，它作为可视化实用程序库，Matplotlib 构建在 NumPy 数组上，旨在与更广泛的 SciPy 堆栈一起工作。
*   **Numpy:** 是一个通用的数组处理包。它提供了高性能多维数组和矩阵以及大量高级数学函数。
*   **mpl_toolkits:** 它提供了一些基本的 3d 绘图(散点、冲浪、线、网格)工具。它是用于在 Matplotlib 中显示 3d 轴的助手类的集合。

### 方法

**步骤 1:** 导入库。

```py
import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d import Axes3D 
import numpy as np
```

**第二步:**在这一步中，我们选择了维度 X =5，Y=5，Z=5 的 3D 轴，在[NP . one()](https://www.geeksforgeeks.org/numpy-ones-python/)中，我们通过了立方体的维度。

```py
# Create axis
axes = [5, 5, 5]

# Create Data
data = np.ones(axes)
```

**步骤 3:** 在这一步中，我们选择颜色不透明度为 alpha = 0.9(从 0.0–1.0 不等)。在下一步中，我们将在 [np.empty()](https://www.geeksforgeeks.org/numpy-empty-python/) 函数中传递立方体的轴的尺寸(即 5，5，5) +面的数量(即 0-4)，然后我们将传递立方体的每个面的颜色组合和不透明度。

```py
# controll Tranperency
alpha = 0.9

# control colour 
colors = np.empty(axes + [4])

colors[0] = [1, 0, 0, alpha] # red
colors[1] = [0, 1, 0, alpha] # green
colors[2] = [0, 0, 1, alpha] # blue
colors[3] = [1, 1, 0, alpha] # yellow
colors[4] = [1, 1, 1, alpha] # grey
```

**第四步:**在这一步中，我们使用了 matplotlib 库的**图()**功能，该功能用于创建一个新的图形，之后，我们使用 **add_subplot()** 方法将一个 Axes 添加到图形中，作为子图排列的三维(即投影= '3d ')部分。它有 3 个参数。

*   Number of rows in the grid,
*   Number of columns in the grid,
*   The location where the new subplots must be placed.

应当注意，图 add _ 子图(1，1，1)等同于图 add _ 子图(111)。

```py
# Plot figure
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
```

**第 5 步:**在最后一步中，体素用于定制尺寸、位置和网格颜色。上面提供了正确的语法。

```py
# Voxels is used to customizations of the 
# sizes, positions and colors.
ax.voxels(data, facecolors=colors, edgecolors='grey')
```

**例 1:一种颜色的简单立方体。**

这里改变**颜色[ : ]** ，意味着我们选择所有的数组元素作为一种颜色(即红色)，为了删除网格，我们从体素方法中删除了“edgecolor”参数，使其只有一个颜色立方体。

## 蟒 3

```py
# Import libraries
import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d import Axes3D
import numpy as np

# Create axis
axes = [5, 5, 5]

# Create Data
data = np.ones(axes, dtype=np.bool)

# Controll Tranperency
alpha = 0.9

# Control colour
colors = np.empty(axes + [4], dtype=np.float32)

colors[:] = [1, 0, 0, alpha]  # red

# Plot figure
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')

# Voxels is used to customizations of the
# sizes, positions and colors.
ax.voxels(data, facecolors=colors)
```
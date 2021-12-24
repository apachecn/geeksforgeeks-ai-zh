# 如何在 Matplotlib 中显示灰度图像？

> 原文:[https://www . geeksforgeeks . org/如何在 matplotlib 中显示灰度图像/](https://www.geeksforgeeks.org/how-to-display-an-image-in-grayscale-in-matplotlib/)

在本文中，我们将使用 *matplotlib* 模块在灰度表示中描绘图像，即仅使用两种颜色即黑色和白色的图像表示。

### **所需模块**

*   [**【PIL】**](https://www.geeksforgeeks.org/python-pillow-a-fork-of-pil/)是 python 图像库，为 Python 解释器提供图像编辑功能。图像模块提供了一个同名的类，用于表示一个 *PIL* 图像。该模块还提供了许多工厂功能，包括从文件加载图像和创建新图像的功能。 *PIL。Image.open()* 方法在 *PIL* 模块中打开并识别给定的图像文件。
*   [**Matplotlib**](https://www.geeksforgeeks.org/python-introduction-matplotlib/) 是一个用 Python 创建静态、动画和交互式可视化的绘图库。 *matplotlib* 模块可用于 Python 脚本、Python 和 IPython 外壳、web 应用服务器以及各种图形用户界面工具包，如 Tkinter、awxPython 等。

**分步方法:**

*   Import required modules

## python 3

```py
# importing libraries.
import numpy as np
import matplotlib.pyplot as plt
from PIL import Image
```
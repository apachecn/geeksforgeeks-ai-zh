# 如何在 Matplotlib 中绘制对数轴？

> 原文:[https://www . geeksforgeeks . org/如何绘制对数轴 in-matplotlib/](https://www.geeksforgeeks.org/how-to-plot-logarithmic-axes-in-matplotlib/)

默认情况下，使用 Matplotlib 的所有图中的“轴”都是线性的， [matplotlib.pyplot](https://www.geeksforgeeks.org/pyplot-in-matplotlib/) 库的 [yscale()](https://www.geeksforgeeks.org/matplotlib-pyplot-yscale-in-python/) 和 [xscale()](https://www.geeksforgeeks.org/matplotlib-pyplot-xscale-function-in-python/) 方法可用于将 y 轴或 x 轴比例分别更改为对数。

yscale()或 xscale()方法将单个值作为一个参数，该参数是刻度的转换类型，为了将轴转换为对数刻度，我们将“log”关键字或 matplotlib.scale. LogScale 类传递给 yscale 或 xscale 方法。

**xscale 方法语法:**

> **语法 ：** matplotlib.pyplot.xscale（value， **kwargs）
> 
> **参数:**
> 
> *   值= {“线性”“对数”“符号对数”“对数”、… }
> *   **kwargs =根据规模(matplotlib.scale.LinearScale、LogScale、SymmetricalLogScale、LogitScale)
> 
> )
> 
> **返回:**将 x 轴转换为给定的比例类型。(这里我们使用“对数”刻度类型)

**yscale 方法语法:**

> ***语法:** matplotlib.pyplot.yscale(值，**kwargs)*
> 
> ***参数:***
> 
> *   ***Value** = {linearity, logarithm, sign logarithm, logit, ...}*
> *   **** * kwargs =** Different keyword parameters are (here we use [logarithmic] scale type)*

下面给出了将 y 轴和 x 轴分别转换为对数刻度的实现。

**例 1:** 无对数轴。

## 蟒 3

```py
import matplotlib.pyplot as plt

# exponential function y = 10^x
data = [10**i for i in range(5)]

plt.plot(data)
```
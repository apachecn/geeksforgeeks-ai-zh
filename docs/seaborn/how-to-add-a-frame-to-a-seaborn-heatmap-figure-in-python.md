# 如何在 Python 中给一个海底热图图添加一帧？

> 原文:[https://www . geesforgeks . org/如何将框架添加到海底-热图-python 中的图形/](https://www.geeksforgeeks.org/how-to-add-a-frame-to-a-seaborn-heatmap-figure-in-python/)

热图是数据的图形表示，其中值用颜色表示。它们使复杂的数据一目了然。使用 python 中的 seaborn 可以轻松绘制热图。在本文中，我们将为 Python 中的海底热图添加一个框架。

> ***语法:** seaborn.heatmap(data，* vmin = None，vmax=None，cmap=None，center=None，annot_kws=None，线宽=0，linecolor='white '，cbar=True，**kwargs)*
> 
> ***重要参数:***
> 
> *   ***Data:** 2D data set that can be forced to be ndarray.*
> *   ***Line width:** The line width of each cell will be divided.*
> *   ***Line color:** The color of the line that will divide each cell.*
> *   ***CBAR:** Whether to draw color bars.*
> 
> *除数据外的所有参数都是可选的。*
> 
> ***返回:**matplotlib . axes . _ 子图类型的对象。axesssubplot*

### **创建热图**

为了绘制热图，我们将使用 seaborn 的内置数据集。Seaborn 有很多内置的数据集，比如 titanic.csv、企鹅. csv、flights.csv、exercise.csv，我们也可以让我们的数据集应该只是一个矩形数组。

## 蟒 3

```
# Import libraries
import seaborn as sns
import matplotlib.pyplot as plt

# Preparing dataset
example = sns.load_dataset("flights")
example = example.pivot("month", "year",
                        "passengers")

# Creating plot
res = sns.heatmap(example)

# show plot
plt.show()
```
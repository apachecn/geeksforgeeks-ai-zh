# 如何用 Python 制作横拉小提琴与海伯恩的剧情？

> 原文:[https://www . geesforgeks . org/how-to-make-horizon-violin-plot-with-seaborn-in-python/](https://www.geeksforgeeks.org/how-to-make-horizontal-violin-plot-with-seaborn-in-python/)

在这篇文章中，我们将与 seaborn 绘制一个水平的 Violin 图。我们可以使用两种方法绘制水平小提琴图，**小提琴图()**和**小提琴图()。**

**方法 1:** 使用[紫花地丁()](https://www.geeksforgeeks.org/violinplot-using-seaborn-in-python/)

一个小提琴情节扮演一个类似的活动，通过触须或方块情节进行。因为它显示了一个或多个分类变量的若干定量数据。在几个单元显示多个数据可能是一种有效且有吸引力的方式。“宽格式”数据框有助于维护可以在图表上绘制的每个数字列。可以使用 NumPy 或 Python 对象，但熊猫对象更好，因为相关名称将用于注释轴。

> **语法:**seaborn . violinplot(x =无，y =无，色相=无，数据=无，scale _ hue =真，**kwargs)
> 
> **参数:**
> **x，y，色相:**用于绘制长格式数据的输入。
> **数据:**用于绘图的数据集。
> **比例:**用来缩放每把小提琴宽度的方法。
> 
> **返回:**该方法返回绘制了绘图的坐标轴对象。

**示例 1:** 仅使用一个轴绘制单个水平图

如果我们只使用一个数据变量，而不是两个数据变量，那么这意味着轴将这些数据变量表示为一个轴。

x 表示 x 轴，y 表示 y 轴。

**语法:**

```
seaborn.violinplot(x)

```

## 蟒蛇 3

```
# Python program to illustrate
# violinplot using inbuilt data-set
# given in seaborn

# importing the required module
import seaborn

# use to set style of background of plot
seaborn.set(style="whitegrid")

# loading data-set
tips = seaborn.load_dataset("tips")

seaborn.violinplot(x=tips["total_bill"])
```
# 蟒蛇熊猫密度图

> 原文:[https://www . geesforgeks . org/density-plot-with-pandas-in-python/](https://www.geeksforgeeks.org/density-plots-with-pandas-in-python/)

密度图是一种数据可视化工具。它是直方图的变体，在绘制值时使用“核平滑”。它是从数据推断出的直方图的连续平滑版本。

密度图使用核密度估计(因此也称为核密度估计图或 KDE)，这是一种概率密度函数。峰值较高的绘图区域是那些值之间存在最大数据点的区域。

密度图可以用熊猫、海鸟等来制作。在本文中，我们将使用熊猫生成密度图。我们将使用西伯恩图书馆的两个数据集，即“车祸”和“提示”。

> *句法:* **熊猫。DataFrame.plot.density |熊猫。DataFrame.plot.kde**
> 
> 其中**熊猫** - >为“熊猫数据框”类型的数据集
> 
> **数据框** - >为其绘制密度图的列
> 
> **绘制** - >关键词指导绘制给定列的图/图形
> 
> **密度** - >用于绘制密度图
> 
> **kde** - >使用核密度估计函数绘制密度图

**示例 1:** 给定数据集“car _ crashes”，让我们使用密度图找出大多数车祸发生的最常见速度。

## 蟒 3

```
# importing the libraries
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# loading the dataset
# from seaborn library
data = sns.load_dataset('car_crashes')

# viewing the dataset
print(data.head(4))
```
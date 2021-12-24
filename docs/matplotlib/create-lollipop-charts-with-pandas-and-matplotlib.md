# 用熊猫和 Matplotlib 创建棒棒糖图表

> 原文:[https://www . geesforgeks . org/create-棒棒糖-charts-with-pandas-and-matplotlib/](https://www.geeksforgeeks.org/create-lollipop-charts-with-pandas-and-matplotlib/)

在本文中，我们将创建**棒棒糖图表**。它们只不过是条形图的一种变体，其中粗条只被一条线和末尾的点状“o”(o 形)所取代。当有大量数据需要表示时，棒棒糖图表是首选的，当以条形表示时，可以形成一个集群。

**链接到 CSV 文件:** [点击这里](https://drive.google.com/file/d/1rpEhCVSytq_AXAiLsXenmrgEAEJOllFC/view?usp=sharing)

让我们用不同的方法讨论一些例子，用熊猫来可视化棒棒糖图表。

**例 1:**

使用 **plt.stem** 功能，它在图表下从基线到 y 的每个 x 位置创建垂直线，并在那里放置一个标记。但是它不够灵活，所以您可能还想尝试其他方法。

在这个例子中，我们将通过使用熊猫从 CSV 文件中收集数据来绘制棒棒糖图表。

首先，我们将通过**PLT . subplts()**创建一个空图表，并使用接受(x，y)形式的参数的主干图，这两个参数都可以是类似数组的值，我们将这些值绘制到图表中。 **use_line_collection=True** 提高了茎图的性能，将茎线绘制为线条集合，而不是单个线条。**基线从茎线上移除基线。**

CSV 文件中有“月 _ 号”和“总 _ 利润”两列，它们是从 CSV 文件中读取的，并作为(x，y)传递到主干图中，还添加了一些格式和细节。

**set_ylim()** 设置为零，y 轴值从零开始。

**方法:**

*   安藤仁介(matplotlib 你好熊猫)
*   Open CSV file and read data
*   使用 PLT。阻止

## python 3

```
# importing modules
from pandas import *
import matplotlib.pyplot as plt

# reading CSV file
d = read_csv("company_sales_data.csv")

# creating an empty chart
fig, axes = plt.subplots()

# plotting using plt.stem
axes.stem(d['month_number'], d['total_profit'],
          use_line_collection=True, basefmt=' ')

# starting value of y-axis
axes.set_ylim(0)

# details and formatting of chart
plt.title('Total Profit')
plt.xlabel('Month')
plt.ylabel('Profit')
plt.xticks(d['month_number'])
```
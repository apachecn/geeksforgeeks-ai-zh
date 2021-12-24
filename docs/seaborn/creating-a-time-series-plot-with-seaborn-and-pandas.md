# 用海鸟和熊猫制作时间序列图

> 原文:[https://www . geesforgeks . org/creating-a-time-series-plot-with-seaborn-and-pandas/](https://www.geeksforgeeks.org/creating-a-time-series-plot-with-seaborn-and-pandas/)

在这篇文章中，我们将学习如何创建一个与海鸟和熊猫的时间序列图。让我们讨论一些概念:

*   **[Panda]** is an open source library based on NumPy library. This is a Python package that provides various data structures and operations to handle numerical data and statistics. Mainly because it is much easier to import and analyze data. Panda's speed and high performance & are productive for users.
*   **seaborn** is a huge visual library for drawing statistical figures in Python. It provides a beautiful default style and palette to form a more attractive statistical chart. It is built at the highest level of matplotlib Library, and is also closely integrated with the information structure of pandas.
*   A **time period** (sometimes called statistical chart) displays the numerical value corresponding to the clock. They are almost like x-y charts, but although x-y charts can plot the distribution of "X" variables (for example, height, weight and age), time batches can only display time on the X axis. Unlike pie charts and bar charts, these charts have no categories. Time batches help to show how data changes over time. For example, if you randomly sample the data, this chart will be very effective.

### 所需步骤

1.  导入包
2.  导入/加载/创建数据。
3.  使用线图绘制数据的时间序列图(因为自 2020 年 9 月以来，tsplot 已被 lineplot 取代)。

### 例子

在这里，我们借助一些例子为理解时间序列图创建一个粗略的数据。让我们创建数据:

```
# importing packages
import pandas as pd

# creating data
df = pd.DataFrame({'Date': ['2019-10-01', '2019-11-01', 
                            '2019-12-01','2020-01-01', 
                            '2020-02-01', '2020-03-01',
                            '2020-04-01', '2020-05-01',
                            '2020-06-01'],

                   'Col_1': [34, 43, 14, 15,
                             15, 14, 31, 25, 62],

                   'Col_2': [52, 66, 78, 15, 15,
                             5, 25, 25, 86],

                   'Col_3': [13, 73, 82, 58, 52,
                             87, 26, 5, 56],

                   'Col_4': [44, 75, 26, 15, 15,
                             14, 54, 25, 24]})

# view dataset
display(df)
```
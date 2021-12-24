# 在 Matplotlib 中显示条形图上方的百分比

> 原文:[https://www . geesforgeks . org/display-percent-over-bar-chart-in-matplotlib/](https://www.geeksforgeeks.org/display-percentage-above-bar-chart-in-matplotlib/)

在本文中，我们将讨论如何使用 Matplotlib 库绘制条形图，并在条形图中的每个条形图上方显示百分比。

为了便于解释，我们将举一个前印度队长 MS Dhoni 在所有模式下得分的例子，然后我们将比较所有模式下得分的得分占他得分总数的百分比。让我们先从导入必要的库开始，然后制作一个包含每种格式的运行记录的数据帧。

## 巨蟒

```py
# import modules
import pandas as pd
import matplotlib.pyplot as plt

# assign data
data = pd.DataFrame({'Format': ['Test', 'ODI', 'T20I', 'IPL'],
                     'Matches': [90, 350, 98, 204],
                     'Runs': [4876, 10773, 1617, 4632]
                     })

# display data
display(data)
```
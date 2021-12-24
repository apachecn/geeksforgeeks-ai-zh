# 如何在熊猫中新增组级汇总统计作为新栏目？

> 原文:[https://www . geeksforgeeks . org/如何添加-组-级别-摘要-统计-作为熊猫中的新列/](https://www.geeksforgeeks.org/how-to-add-group-level-summary-statistic-as-a-new-column-in-pandas/)

在本文中，我们将学习如何在数据框熊猫中添加组级摘要统计作为新列。这可以通过使用统计平均值、模式等概念来实现。这需要以下步骤:

1.  Select a data frame.
2.  Form statistical data from a column or group of columns.
3.  Store data as a series
4.  Add the series in the data frame as a column.

这里，我们取一个数据框，数据框由学生证、姓名、分数和成绩组成。让我们创建数据框

```py
# importing packages
import pandas as pd

# dictionary of data
dct = {'ID': {0: 23, 1: 43, 2: 12,
              3: 13, 4: 67, 5: 89,
              6: 90, 7: 56, 8: 34},

       'Name': {0: 'Ram', 1: 'Deep',
                2: 'Yash', 3: 'Aman',
                4: 'Arjun', 5: 'Aditya',
                6: 'Divya', 7: 'Chalsea',
                8: 'Akash'},

       'Marks': {0: 89, 1: 97, 2: 45, 3: 78,
                 4: 56, 5: 76, 6: 100, 7: 87,
                 8: 81},

       'Grade': {0: 'B', 1: 'A', 2: 'F', 3: 'C',
                 4: 'E', 5: 'C', 6: 'A', 7: 'B',
                 8: 'B'}
       }

# create dataframe
df = pd.DataFrame(dct)

# view dataframe
df
```
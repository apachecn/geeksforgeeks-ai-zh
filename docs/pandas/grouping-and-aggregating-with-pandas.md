# 与熊猫分组和聚集

> 原文:[https://www . geeksforgeeks . org/与熊猫分组和聚合/](https://www.geeksforgeeks.org/grouping-and-aggregating-with-pandas/)

在本文中，我们将看到使用熊猫进行分组和聚合。分组和聚合将有助于使用各种功能轻松实现数据分析。这些方法将帮助我们分组和总结我们的数据，并使复杂的分析相对容易。

**创建各种主题的标记样本数据集。**

## 巨蟒

```py
# import module
import pandas as pd

# Creating our dataset
df = pd.DataFrame([[9, 4, 8, 9],
                   [8, 10, 7, 6],
                   [7, 6, 8, 5]],
                  columns=['Maths',  'English', 
                           'Science', 'History'])

# display dataset
print(df)
```
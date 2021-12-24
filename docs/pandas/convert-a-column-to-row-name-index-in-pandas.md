# 将熊猫中的列转换为行名称/索引

> 原文:[https://www . geesforgeks . org/convert-a-column-to-row-name-index-in-pandas/](https://www.geeksforgeeks.org/convert-a-column-to-row-name-index-in-pandas/)

熊猫提供了一种处理数据及其转换的便捷方式。让我们看看如何在 Pandas 中将一列转换为行名/索引。

首先用列表字典创建一个数据框架。

## 蟒 3

```
# importing pandas as pd
import pandas as pd

# Creating a dict of lists
data = {'Name':["Akash", "Geeku", "Pankaj", "Sumitra","Ramlal"],
       'Branch':["B.Tech", "MBA", "BCA", "B.Tech", "BCA"],
       'Score':["80","90","60", "30", "50"],
       'Result': ["Pass","Pass","Pass","Fail","Fail"]}

# creating a dataframe
df = pd.DataFrame(data)

df
```
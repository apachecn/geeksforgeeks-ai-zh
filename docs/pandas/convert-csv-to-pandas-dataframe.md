# 将 CSV 转换为熊猫数据帧

> 原文:[https://www . geesforgeks . org/convert-CSV-to-pandas-data frame/](https://www.geeksforgeeks.org/convert-csv-to-pandas-dataframe/)

在本文中，我们将讨论如何将 csv 转换为 Pandas Dataframe，这个操作可以使用 [pandas.read_csv](https://www.geeksforgeeks.org/python-read-csv-using-pandas-read_csv/) 将逗号分隔值(CSV)文件读入 Dataframe。

**示例 1:** 在下面的程序中，我们将把 [nba.csv](https://media.geeksforgeeks.org/wp-content/uploads/nba.csv) 转换成数据帧，然后显示出来。

## 蟒蛇

```py
# import pandas module 
import pandas as pd 

# making dataframe 
df = pd.read_csv("nba.csv") 

# output the dataframe
print(df)
```
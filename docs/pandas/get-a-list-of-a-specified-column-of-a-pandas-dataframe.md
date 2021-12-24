# 获取熊猫数据框指定列的列表

> 原文:[https://www . geesforgeks . org/get-a-list-a-specified-column-a-pandas-data frame/](https://www.geeksforgeeks.org/get-a-list-of-a-specified-column-of-a-pandas-dataframe/)

在本文中，我们将讨论如何获取一个[熊猫数据帧的指定列的列表。](https://www.geeksforgeeks.org/python-pandas-dataframe/)首先，我们将把一个 csv 文件读入熊猫的数据帧。

**注意:**要获取使用的 CSV 文件，请点击此处。
**例:**

## 蟒蛇 3

```py
# importing pandas module 
import pandas as pd 

# making data frame from csv
data = pd.read_csv("nba.csv") 

# calling head() method  
df = data.head(5) 

# displaying data 
df
```
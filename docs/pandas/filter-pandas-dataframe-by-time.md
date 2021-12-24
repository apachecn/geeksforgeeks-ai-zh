# 按时间过滤熊猫数据帧

> 原文:[https://www . geesforgeks . org/filter-pandas-data frame by time/](https://www.geeksforgeeks.org/filter-pandas-dataframe-by-time/)

在本文中，让我们看看如何按日期过滤熊猫数据帧。因此，我们可以使用逻辑运算符和 [loc()](https://www.geeksforgeeks.org/python-pandas-dataframe-loc/) 方法按日期过滤 python pandas 数据帧。在下面的示例中，我们有一个包含两列的数据框，第一列是名称，另一列是 DOB。

**例 1:** 过滤数据，其 DOB 大于1999-02-5。

## 蟒蛇

```py
import pandas as pd

# create data frame
Data = {'Name': ['Mukul', 'Rohan', 'Mayank',
                          'Shubham', 'Aakash'],

        'DOB': ['1997-04-24', '1998-05-25', '1999-04-11',
                '2000-11-15', '1998-06-28']}

df = pd.DataFrame(Data)

# print original data frame
print(df)

# filter data frame
New_df = df.loc[df["DOB"] >= "1999-02-5"]

# print filtered data frame
print(New_df)
```
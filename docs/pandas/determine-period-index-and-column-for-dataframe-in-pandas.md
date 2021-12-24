# 确定熊猫数据帧的周期指数和栏数

> 原文:[https://www . geesforgeks . org/确定熊猫数据框的周期索引和列/](https://www.geeksforgeeks.org/determine-period-index-and-column-for-dataframe-in-pandas/)

在 Pandas 确定数据框的周期索引和列中，我们将使用 [pandas.period_range()](https://www.geeksforgeeks.org/python-pandas-period_range-method/) 方法。这是 Pandas 中的常规函数之一，用于返回固定频率的周期索引，默认频率为日(日历)。

> ***语法:** pandas.to_numeric(arg，errors='raise '，downcast=None)*
> 
> ***参数:***
> ***开始:**左界为生成期间*
> ***结束:**右界为生成期间*
> ***期间:**要生成的期间数*
> ***freq :** 频率别名*
> **名称:**生成的期间索引的名称
> 
> ***返回:**周期指数*

**例 1:**

## 蟒蛇 3

```py
import pandas as pd

course = ["DBMS", "DSA", "OOPS",
          "System Design", "CN", ]

# pass the period and starting index
webinar_date = pd.period_range('2020-08-15', periods=5)

# Determine Period Index and Column
# for DataFrame
df = pd.DataFrame(course, index=webinar_date, columns=['Course'])

df
```
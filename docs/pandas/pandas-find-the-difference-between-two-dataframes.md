# 熊猫——找出两个数据帧的区别

> 原文:[https://www . geesforgeks . org/pandas-找到两个数据框的区别/](https://www.geeksforgeeks.org/pandas-find-the-difference-between-two-dataframes/)

在本文中，我们将讨论如何比较熊猫的两个数据帧。首先，让我们创建两个数据帧。

**创建两个数据框**

## python 3

```
import pandas as pd

# first dataframe
df1 = pd.DataFrame({
    'Age': ['20', '14', '56', '28', '10'],
    'Weight': [59, 29, 73, 56, 48]})
display(df1)

# second dataframe
df2 = pd.DataFrame({
    'Age': ['16', '20', '24', '40', '22'],
    'Weight': [55, 59, 73, 85, 56]})
display(df2)
```
# 如何在熊猫数据框行中搜索一个值？

> 原文:[https://www . geesforgeks . org/how-search-a-value-in-pandas-data frame-row/](https://www.geeksforgeeks.org/how-to-search-a-value-within-a-pandas-dataframe-row/)

在本文中，我们将看到如何在 Python 的 Pandas DataFrame 行中搜索一个值。

### 导入**库**和数据

在这里，我们将导入所需的模块，然后将数据文件作为 dataframe 读取。

使用的数据集链接在这里是

## 蟒蛇 3

```py
# importing pandas as ps
import pandas as pd

# importing data using .read_csv() method
df = pd.read_csv("data.csv")
```

**输出:**

![](img/bed136904cf72702dd0020478f08c891.png)

### 搜索值

这里我们将在 dataframe 中搜索列名。

> **语法**:df[df[' column _ name ']= = value _ you _ are _ look _ for]
> 
> 其中 df 是我们的数据帧

我们将在“已购买”列中搜索所有值为“是”的行。

## 蟒蛇 3

```py
df[df["Purchased"] == "Yes"]
# This line of code will print all rows
# which satisfy the condition df["Purchased"] == "Yes"

# In other words df["Purchased"] == "Yes"
# will return a boolean either true or false.

# if it returns true then we will print that
# row otherwise we will not print the row.
```
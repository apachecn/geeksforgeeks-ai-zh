# 如何将熊猫数据框中的索引转换为列？

> 原文:[https://www . geesforgeks . org/如何将索引转换为熊猫中的列-dataframe/](https://www.geeksforgeeks.org/how-to-convert-index-to-column-in-pandas-dataframe/)

[**【熊猫】**](https://www.geeksforgeeks.org/introduction-to-pandas-in-python/) 是一个强大的工具，用于数据分析，建立在 python 库之上。熊猫库使用户能够有效地创建和操作数据框架(数据表)和时间序列。这些数据帧可用于训练和测试机器学习模型以及分析数据。

## 将索引转换为列

默认情况下，数据框的每一行都有一个索引值。数据框中的行按顺序被分配从 0 到(行数–1)的索引值，每行有一个索引值。有许多方法可以将索引转换为熊猫数据框中的一列。让我们创建一个数据帧。

## 蟒 3

```py
# importing the pandas library as pd
import pandas as pd

# Creating the dataframe df
df = pd.DataFrame({'Roll Number': ['20CSE29', '20CSE49', '20CSE36', '20CSE44'],
                   'Name': ['Amelia', 'Sam', 'Dean', 'Jessica'],
                   'Marks In Percentage': [97, 90, 70, 82],
                   'Grade': ['A', 'A', 'C', 'B'],
                   'Subject': ['Physics', 'Physics', 'Physics', 'Physics']})

# Printing the dataframe
df
```
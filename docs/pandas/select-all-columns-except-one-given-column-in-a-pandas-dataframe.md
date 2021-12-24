# 选择除熊猫数据框中一个给定列之外的所有列

> 原文:[https://www . geesforgeks . org/select-all-columns-除了一个给定的熊猫中的一列-dataframe/](https://www.geeksforgeeks.org/select-all-columns-except-one-given-column-in-a-pandas-dataframe/)

[**数据框架**](https://www.geeksforgeeks.org/python-pandas-dataframe/) 数据结构是熊猫库的心脏。数据框基本上是二维系列对象。它们有行和列，行代表索引，列代表内容。现在，让我们看看如何选择除熊猫数据框中一个给定列之外的所有列。

首先，让我们创建一个数据框:

## python 3

```py
# import pandas library
import pandas as pd

# create a Dataframe
data = pd.DataFrame({
    'course_name': ['Data Structures', 'Python',
                    'Machine Learning'],
    'student_name': ['A', 'B', 
                     'C'],
    'student_city': ['Chennai', 'Pune', 
                     'Delhi'],
    'student_gender': ['M', 'F',
                       'M'] })
# show the Dataframe
data
```
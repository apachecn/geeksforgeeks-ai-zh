# 在熊猫

中给数据框添加多列

> 原文:[https://www . geeksforgeeks . org/add-多列转熊猫数据框/](https://www.geeksforgeeks.org/add-multiple-columns-to-dataframe-in-pandas/)

在 Pandas 中，我们可以随时在数据框中添加列。有多种方法可以将列添加到熊猫数据框中。

**方法 1:** 使用**列表**

## python 3

向数据框添加多列

```
# importing pandas library
import pandas as pd

# creating and initializing a nested list
students = [['jackma', 34, 'Sydeny', 'Australia'],
            ['Ritika', 30, 'Delhi', 'India'],
            ['Vansh', 31, 'Delhi', 'India'],
            ['Nany', 32, 'Tokyo', 'Japan'],
            ['May', 16, 'New York', 'US'],
            ['Michael', 17, 'las vegas', 'US']]

# Create a DataFrame object
df = pd.DataFrame(students,
                  columns=['Name', 'Age', 'City', 'Country'],
                  index=['a', 'b', 'c', 'd', 'e', 'f'])

# Creating 2 lists 'marks' and 'gender'
marks = [85.4,94.9,55.2,100.0,40.5,33.5]
gender = ['M','F','M','F','F','M']

# adding lists as new column to dataframe df
df['Uni_Marks'] = marks
df['Gender'] = gender

# Displaying the Data frame
df
```
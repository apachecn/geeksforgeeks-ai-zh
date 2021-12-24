# 在熊猫的现有数据框中添加新列

> 原文:[https://www . geesforgeks . org/向现有熊猫数据框添加新列/](https://www.geeksforgeeks.org/adding-new-column-to-existing-dataframe-in-pandas/)

让我们讨论如何在 Pandas 中向现有的数据框架添加新列。我们有多种方法可以完成这项任务。

**方法#1:** 通过将一个新列表声明为一列。

## 蟒 3

```py
# Import pandas package
import pandas as pd

# Define a dictionary containing Students data
data = {'Name': ['Jai', 'Princi', 'Gaurav', 'Anuj'],
        'Height': [5.1, 6.2, 5.1, 5.2],
        'Qualification': ['Msc', 'MA', 'Msc', 'Msc']}

# Convert the dictionary into DataFrame
df = pd.DataFrame(data)

# Declare a list that is to be converted into a column
address = ['Delhi', 'Bangalore', 'Chennai', 'Patna']

# Using 'Address' as the column name
# and equating it to the list
df['Address'] = address

# Observe the result
df
```
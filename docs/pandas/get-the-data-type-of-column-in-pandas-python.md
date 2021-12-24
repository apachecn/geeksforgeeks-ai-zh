# 获取熊猫 Python 中列的数据类型

> 原文:[https://www . geesforgeks . org/get-the-data-type-in-pandas-python/](https://www.geeksforgeeks.org/get-the-data-type-of-column-in-pandas-python/)

让我们看看如何在 [**熊猫数据框**](https://www.geeksforgeeks.org/python-pandas-dataframe/) 中获取列的数据类型。首先，让我们创建一个熊猫数据框架。

**例:**

## 蟒 3

```py
# importing pandas library
import pandas as pd

# List of Tuples
employees = [
            ('Stuti', 28, 'Varanasi', 20000),
            ('Saumya', 32, 'Delhi', 25000),
            ('Aaditya', 25, 'Mumbai', 40000),
            ('Saumya', 32, 'Delhi', 35000),
            ('Saumya', 32, 'Delhi', 30000),
            ('Saumya', 32, 'Mumbai', 20000),
            ('Aaditya', 40, 'Dehradun', 24000),
            ('Seema', 32, 'Delhi', 70000)
            ]

# Create a DataFrame
df = pd.DataFrame(employees,
                  columns = ['Name', 'Age',
                             'City', 'Salary'])
# show the dataframe
df
```
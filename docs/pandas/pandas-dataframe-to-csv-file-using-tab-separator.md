# 熊猫–使用制表符分隔符

将数据框转换为 CSV 文件

> 原文:[https://www . geesforgeks . org/pandas-data frame-to-CSV-file-using-tab-separator/](https://www.geeksforgeeks.org/pandas-dataframe-to-csv-file-using-tab-separator/)

让我们看看如何使用标签分隔符将数据帧转换为 CSV 文件。我们将使用[到 _csv()](https://www.geeksforgeeks.org/saving-a-pandas-dataframe-as-a-csv/) 方法将数据帧保存为 csv 文件。要保存带有制表符分隔符的 DataFrame，我们必须在 to_csv()方法中传递“\t”作为 sep 参数。

**方法:**

1.  Import panda and Numpy modules.
2.  Use DataFrame () method to create a data frame.
3.  Use the to_csv () method with sep as parameter "\t" to save the data frame as a csv file.
4.  Use the read_csv () method as DataFrame to load the newly created CSV file.
5.  Show a new data frame.

## 蟒 3

```py
# importing the modules
import pandas as pd
import numpy as np

# creating a DataFrame
students = {'Student': ['Amit', 'Cody',
                        'Darren', 'Drew'],
            'RollNumber': [1, 5, 10, 15],
            'Grade': ['A', 'C', 'F', 'B']}
df = pd.DataFrame(students,
                  columns =['Student', 'RollNumber',
                            'Grade'])
# displaying the original DataFrame
print("Original DataFrame")
print(df)

# saving as a CSV file
df.to_csv('Students.csv', sep ='\t')

# loading the CSV file
new_df = pd.read_csv('Students.csv')

# displaying the new DataFrame
print('Data from Students.csv:')
print(new_df)
```
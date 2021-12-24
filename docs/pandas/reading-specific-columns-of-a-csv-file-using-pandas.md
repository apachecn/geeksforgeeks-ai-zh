# 使用熊猫读取 CSV 文件的特定列

> 原文:[https://www . geesforgeks . org/reading-specific-columns-of-a-CSV-file-use-pandas/](https://www.geeksforgeeks.org/reading-specific-columns-of-a-csv-file-using-pandas/)

让我们看看如何使用 Pandas 读取 CSV 文件的特定列。这可以借助[**熊猫 _csv()**](https://www.geeksforgeeks.org/python-read-csv-using-pandas-read_csv/) 的方法来完成。我们将第一个参数作为 CSV 文件传递，第二个参数作为关键字**中特定列的列表传递。它将返回特定列的 CSV 文件的数据。**

**示例** **1:** 所用 CSV 文件的链接:[链接](https://drive.google.com/file/d/1keaXQTUztdDO-x-U07NasuYyczhheKZR/view?usp=sharing)

## python 3

```py
# importing the module
import pandas as pd

# read specific columns of csv file using Pandas
df = pd.read_csv("student_scores2.csv", usecols = ['IQ','Scores'])
print(df)
```
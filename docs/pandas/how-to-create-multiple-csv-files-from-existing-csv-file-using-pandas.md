# 如何使用 Pandas 从现有 CSV 文件创建多个 CSV 文件？

> 原文:[https://www . geeksforgeeks . org/如何从现有的 csv 文件创建多个 csv 文件使用熊猫/](https://www.geeksforgeeks.org/how-to-create-multiple-csv-files-from-existing-csv-file-using-pandas/)

在本文中，我们将学习如何使用 Pandas 从现有的 CSV 文件创建多个 CSV 文件。当我们将代码输入生产时，我们将需要处理编辑数据文件。由于数据文件很大，我们会遇到更多的问题，所以我们根据一些标准将这个文件分成一些小文件，比如分成行、列、列的特定值等。

首先，让我们创建一个简单的 CSV 文件，并将其用于本文下面的所有示例。使用 pandas 的 dataframe 方法创建数据集，然后将其保存到“Customers.csv”文件中，或者我们可以使用 Pandas read_csv()函数加载现有数据集。

## 蟒 3

```
import pandas as pd

# initialise data dictionary.
data_dict = {'CustomerID': [1, 2, 3, 4, 5, 6, 7, 8, 9, 10],

             'Gender': ["Male", "Female", "Female", "Male",
                        "Male", "Female", "Male", "Male",
                        "Female", "Male"],

             'Age': [20, 21, 19, 18, 25, 26, 32, 41, 20, 19],

             'Annual Income(k$)': [10, 20, 30, 10, 25, 60, 70,
                                   15, 21, 22],

             'Spending Score': [30, 50, 48, 84, 90, 65, 32, 46,
                                12, 56]}

# Create DataFrame
data = pd.DataFrame(data_dict)

# Write to CSV file
data.to_csv("Customers.csv")

# Print the output.
print(data)
```
# 熊猫 VS NumPy 的区别

> 原文:[https://www . geesforgeks . org/difference-pandas-vs-numpy/](https://www.geeksforgeeks.org/difference-between-pandas-vs-numpy/)

[**熊猫**](https://www.geeksforgeeks.org/pandas-tutorial/) **:** It 是一个开源的、BSD 许可的库，用 *Python* 语言编写。*熊猫*提供高性能、快速、易用的数据结构和数据分析工具，用于操作数字数据和时间序列。*熊猫*建立在 *numpy* 库的基础上，用像*Python**Cython*和 *C* 这样的语言编写。在熊猫中，我们可以从 *JSON、SQL、微软 Excel、*等各种文件格式导入数据。

**例:**

## 蟒 3

```
# Importing pandas library
import pandas as pd

# Creating and initializing a nested list
age = [['Aman', 95.5, "Male"], ['Sunny', 65.7, "Female"],
       ['Monty', 85.1, "Male"], ['toni', 75.4, "Male"]]

# Creating a pandas dataframe
df = pd.DataFrame(age, columns=['Name', 'Marks', 'Gender'])

# Printing dataframe
df
```
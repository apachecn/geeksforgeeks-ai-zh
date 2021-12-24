# 如何转换熊猫数据框一列的索引？

> 原文:[https://www . geeksforgeeks . org/如何转换熊猫专栏索引-数据框/](https://www.geeksforgeeks.org/how-to-convert-index-in-a-column-of-the-pandas-dataframe/)

数据框中的每一行(即级别=0)都有一个索引值，即从 0 到 n-1 索引位置的值，有许多方法可以将这些索引值转换为熊猫数据框中的一列。首先，让我们创建一个熊猫数据框架。在这里，我们将创建一个熊猫数据框架，关于学生在特定科目中的分数，包括卷号、姓名、分数、年级和科目。

**例:**

## 蟒 3

```
# importing the pandas library as pd
import pandas as pd    

# Creating the dataframe Ab
AB = pd.DataFrame({'Roll Number': ['9917102206', '9917102250',
                                   '9917102203', '9917102204',
                                   '9917102231'],
                   'Name': ['TANYA', 'PREETIKA', 'KUSHAGRA',
                            'PRAKHAR','ASHISH'],
                   'Score': [99, 98, 50, 45,97],
                   'Grade': ['A+', 'A+', 'C+', 'C','A'],
                   'Subject': ['Operating Systems', 'Operating Systems',
                               'Operating Systems', 'Operating Systems',
                               'Operating Systems']})

# Printing the dataframe
AB
```
# 如何用 Python 把熊猫数据框写成 TSV？

> 原文:[https://www . geeksforgeeks . org/怎么写-pandas-data frame-as-tsv-using-python/](https://www.geeksforgeeks.org/how-to-write-pandas-dataframe-as-tsv-using-python/)

在本文中，我们将讨论如何使用 Python 将熊猫数据框写成 TSV。

让我们从创建数据框开始。这可以通过导入现有文件来完成，但是为了简单起见，我们将创建自己的文件。

## 蟒 3

```py
# importing the module
import pandas as pd

# creating some sample data
sample = {'name': ['a', 'b', 'c', 'd'],
         'age': [24, 65, 39, 18]}

# creating the DataFrame
df = pd.DataFrame(sample)

# displaying the DataFrame
print(df)
```
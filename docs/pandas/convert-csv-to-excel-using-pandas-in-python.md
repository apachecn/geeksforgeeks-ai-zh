# 用 Python 熊猫把 CSV 转换成 Excel】

> 原文:[https://www . geeksforgeeks . org/convert-CSV-to-excel-using-pandas-in-python/](https://www.geeksforgeeks.org/convert-csv-to-excel-using-pandas-in-python/)

熊猫可以读取、过滤和重新排列大小数据集，并以包括 Excel 在内的一系列格式输出它们。在本文中，我们将讨论。csv 文件导入 excel(。xlsx)。

熊猫提供了 ExcelWriter 类，用于将数据框对象写入 excel 工作表。
**语法:**

```py
final = pd.ExcelWriter('GFG.xlsx')

```

**示例:**

**CSV 文件样本:**

![python-csv-to-json](img/f23ab1f954c303b7a022536e23acd2e9.png)

```py
import pandas as pd
import numpy as np

# Reading the csv file
df_new = pd.read_csv('Names.csv')

# saving xlsx file
GFG = pd.ExcelWriter('Names.xlsx')
df_new.to_excel(GFG, index = False)

GFG.save()
```

**输出:**

![python-csv-to-excel](img/5c82fd6799253cf940545bc99225b8bc.png)
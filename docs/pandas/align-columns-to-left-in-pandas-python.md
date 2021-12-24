# 在熊猫 Python 中向左对齐列

> 原文:[https://www . geesforgeks . org/align-columns-to-left-in-pandas-python/](https://www.geeksforgeeks.org/align-columns-to-left-in-pandas-python/)

Pandas 库对于在 Python 中执行探索性数据分析非常有用。熊猫数据框以表格形式表示数据。我们可以对数据执行操作并显示它。在本文中，我们将在 Pandas 中向左对齐列。当显示数据框时，我们可以将列中的数据左对齐、右对齐或居中对齐。

**默认为右对齐，如下例所示。**

## 蟒 3

```
# Python code demonstrate creating
# DataFrame from dict and left aligning
import pandas as pd

# initialise data of lists.
data = {'Name' : ['Tania', 'Ravi',
                  'Surbhi', 'Ganesh'],

        'Articles' : [50, 30, 45, 33],

        'Location' : ['Kanpur', 'Kolkata',
                      'Kolkata', 'Bombay']}

# Create DataFrame
df = pd.DataFrame(data)
display(df)
```
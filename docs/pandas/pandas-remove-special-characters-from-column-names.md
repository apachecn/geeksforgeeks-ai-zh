# 熊猫–删除列名中的特殊字符

> 原文:[https://www . geesforgeks . org/pandas-从列名中删除特殊字符/](https://www.geeksforgeeks.org/pandas-remove-special-characters-from-column-names/)

让我们看看如何删除特殊字符，如#、@、&等。熊猫数据框中的列名。这里我们将使用替换功能来删除特殊字符。

**示例 1:** 从列名中删除特殊字符

## 【Python】

```
# import pandas
import pandas as pd

# create data frame
Data = {'Name#': ['Mukul', 'Rohan', 'Mayank',
                  'Shubham', 'Aakash'],

        'Location': ['Saharanpur', 'Meerut', 'Agra',
                     'Saharanpur', 'Meerut'],

        'Pay': [25000, 30000, 35000, 40000, 45000]}

df = pd.DataFrame(Data)

# print original data frame
print(df)

# remove special character
df.columns = df.columns.str.replace('[#,@,&]', '')

# print file after removing special character
print("\n\n", df)
```
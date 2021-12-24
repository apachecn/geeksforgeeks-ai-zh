# 取消熊猫中列名的空格

> 原文:[https://www . geeksforgeeks . org/从熊猫名称栏中删除空格/](https://www.geeksforgeeks.org/remove-spaces-from-column-names-in-pandas/)

从 pandas 的列名中删除空格并不难，我们可以使用 replace()函数轻松地从 pandas 的列名中删除空格。我们也可以用另一个字符替换空格。让我们一个接一个地看两者的例子。

**示例 1:** 从列名

## Python

中删除空格

```
# import pandas
import pandas as pd

# create data frame
Data = {'Employee Name': ['Mukul', 'Rohan', 'Mayank',
                          'Shubham', 'Aakash'],

        'Location': ['Saharanpur', 'Meerut', 'Agra', 
                     'Saharanpur', 'Meerut'],

        'Sales Code': ['muk123', 'roh232', 'may989',
                       'shu564', 'aka343']}

df = pd.DataFrame(Data)

# print original data frame
print(df)

# remove special character
df.columns = df.columns.str.replace(' ', '')

# print file after removing special character
print("\n\n", df)
```
# 洗牌给定熊猫数据帧行

> 原文:[https://www . geesforgeks . org/shuffle-给定熊猫-data frame-row/](https://www.geeksforgeeks.org/shuffle-a-given-pandas-dataframe-rows/)

让我们看看如何打乱数据帧的行。我们将使用 pandas 模块的[示例()](https://www.geeksforgeeks.org/python-pandas-dataframe-sample/)方法随机打乱 Pandas 中的数据帧行。

**例 1:**

## 蟒 3

```py
# import the module
import pandas as pd

# create a DataFrame
data = {'Name': ['Mukul', 'Rohan', 'Mayank',
                 'Shubham', 'Aakash'],
        'Class': ['BCA', 'BBA', 'BCA', 'MBA', 'BBA'],
        'Location' : ['Saharanpur', 'Meerut', 'Agra',
                      'Saharanpur', 'Meerut']}
df1 = pd.DataFrame(data)

# print the original DataFrame
print("Original DataFrame :")
display(df1)

# shuffle the DataFrame rows
df2 = df1.sample(frac = 1)

# print the shuffled DataFrame
print("\nAfter Shuffle:")
display(df2)
```
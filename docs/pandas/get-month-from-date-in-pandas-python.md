# 从熊猫-蟒蛇日期开始获取月份

> 原文:[https://www . geesforgeks . org/get-月初熊猫-python/](https://www.geeksforgeeks.org/get-month-from-date-in-pandas-python/)

**[【熊猫】](https://www.geeksforgeeks.org/introduction-to-pandas-in-python/)** 有许多内置的方法，可以用来从给定日期中提取月份，这些方法是使用**随机**函数随机生成的，或者使用**时间戳**函数生成的，或者使用**到 _datetime** 函数转换为日期格式的。让我们看几个例子来更好地理解。

**例 1**

```
import pandas as pd

dti = pd.date_range('2020-07-01', periods = 4, freq ='M')
print(dti.month)
```

**输出:**

```
Int64Index([7, 8, 9, 10], dtype='int64')

```
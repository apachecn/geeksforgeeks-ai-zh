# Python | Pandas series . dt . is _ quarter _ start

> 原文:[https://www . geesforgeks . org/python-pandas-series-dt-is _ quarter _ start/](https://www.geeksforgeeks.org/python-pandas-series-dt-is_quarter_start/)

`Series.dt`可用于访问系列的值，如 datetimelike，并返回几个属性。熊猫 `**Series.dt.is_quarter_start**`属性返回一个布尔值，指示日期是否是一个季度的第一天。

> **语法:** Series.dt.is_quarter_start
> 
> **参数:**无
> 
> **返回:** numpy 数组

**示例#1:** 使用`Series.dt.is_quarter_start`属性检查给定系列对象的基础数据中的日期是否是季度的第一天。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series(['2012-4-1', '2019-7-18 12:30', '2008-02-2 10:30',
               '2010-4-22 09:25', '2019-1-1 00:00'])

# Creating the index
idx = ['Day 1', 'Day 2', 'Day 3', 'Day 4', 'Day 5']

# set the index
sr.index = idx

# Convert the underlying data to datetime 
sr = pd.to_datetime(sr)

# Print the series
print(sr)
```

**输出:**
![](img/071c13f87c65832fe3caed0fd85a20a3.png)

现在我们将使用`Series.dt.is_quarter_start`属性来检查给定序列对象中的日期是否是季度的第一天。

```py
# check if dates are the first
# day of the quarter
result = sr.dt.is_quarter_start

# print the result
print(result)
```

**输出:**
![](img/6a073f31036bc3e0d9528032968ab52e.png)
正如我们在输出中看到的，`Series.dt.is_quarter_start`属性已经成功访问并返回了指示日期是否是季度的第一天的布尔值。

**示例 2 :** 使用`Series.dt.is_quarter_start`属性检查给定序列对象的基础数据中的日期是否是季度的第一天。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series(pd.date_range('2012-4-1 00:00',
                    periods = 5, freq = 'W'))

# Creating the index
idx = ['Day 1', 'Day 2', 'Day 3', 'Day 4', 'Day 5']

# set the index
sr.index = idx

# Print the series
print(sr)
```

**输出:**
![](img/8d0bec38becefdc2f49d5ff70a8cc23b.png)

现在我们将使用`Series.dt.is_quarter_start`属性来检查给定序列对象中的日期是否是季度的第一天。

```py
# check if dates are the first
# day of the quarter
result = sr.dt.is_quarter_start

# print the result
print(result)
```

**输出:**
![](img/28b09ea3a2bc37b601980d2412873677.png)

正如我们在输出中看到的那样，`Series.dt.is_quarter_start`属性已经成功访问并返回了布尔值，指示日期是否是季度的第一天。
# Python | Pandas series . dt . is _ year _ start

> 原文:[https://www . geesforgeks . org/python-pandas-series-dt-is _ year _ start/](https://www.geeksforgeeks.org/python-pandas-series-dt-is_year_start/)

`Series.dt`可用于访问系列的值，如 datetimelike，并返回几个属性。熊猫 `**Series.dt.is_year_start**`属性返回一个布尔值，指示日期是否是一年的第一天。

> **语法:** Series.dt.is_year_start
> 
> **参数:**无
> 
> **返回:** numpy 数组

**示例#1:** 使用`Series.dt.is_year_start`属性检查给定序列对象的基础数据中的日期是否是一年的第一天。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series(['2012-3-31', '2019-1-1 12:30', '2008-02-2 10:30',
               '2010-1-1 09:25', '2019-12-31 00:00'])

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
![](img/2d2b69e7e2cf103a6652c252ff155141.png)

现在我们将使用`Series.dt.is_year_start`属性来检查给定序列对象中的日期是否是一年的第一天。

```py
# check if dates are the
# first day of a year
result = sr.dt.is_year_start

# print the result
print(result)
```

**输出:**
![](img/e0feb3a1e381dbace4a9180718b90cd8.png)
正如我们在输出中看到的，`Series.dt.is_year_start`属性已经成功访问并返回了指示日期是否是一年的第一天的布尔值。

**例 2 :** 使用`Series.dt.is_year_start`属性检查给定序列对象的基础数据中的日期是否是一年的第一天。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series(pd.date_range('2012-1-1 00:00', periods = 5, freq = 'D'))

# Creating the index
idx = ['Day 1', 'Day 2', 'Day 3', 'Day 4', 'Day 5']

# set the index
sr.index = idx

# Print the series
print(sr)
```

**输出:**
![](img/115e823199e2da420a75ce8558c55ddf.png)

现在我们将使用`Series.dt.is_year_start`属性来检查给定序列对象中的日期是否是一年的第一天。

```py
# check if dates are the
# first day of a year
result = sr.dt.is_year_start

# print the result
print(result)
```

**输出:**
![](img/07a007606d72f62cd1127cdcda109f9c.png)
正如我们在输出中看到的，`Series.dt.is_year_start`属性已经成功访问并返回了指示日期是否是一年的第一天的布尔值。
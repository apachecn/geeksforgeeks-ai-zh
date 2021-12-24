# Python | Pandas series . dt . is _ year _ end

> 原文:[https://www . geesforgeks . org/python-pandas-series-dt-is _ year _ end/](https://www.geeksforgeeks.org/python-pandas-series-dt-is_year_end/)

`Series.dt`可用于访问系列的值，如 datetimelike，并返回几个属性。熊猫 `**Series.dt.is_year_end**`属性返回一个布尔值，指示日期是否是一年的最后一天。

> **语法:** Series.dt.is_year_end
> 
> **参数:**无
> 
> **返回:** numpy 数组

**示例#1:** 使用`Series.dt.is_year_end`属性检查给定序列对象的基础数据中的日期是否是一年的最后一天。

```
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series(['2012-12-31', '2019-1-1 12:30', '2008-02-2 10:30',
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

![](img/d78f036d93937c0d2308be4cace65f1c.png)

现在我们将使用`Series.dt.is_year_end`属性来检查给定序列对象中的日期是否是一年的最后一天。

```
# check if dates are the
# last day of a year
result = sr.dt.is_year_end

# print the result
print(result)
```

**输出:**

![](img/01b97c543c4084ba7454a0235e6109d9.png)

正如我们在输出中看到的那样，`Series.dt.is_year_end`属性已经成功访问并返回了指示日期是否是一年的最后一天的布尔值。

**示例 2 :** 使用`Series.dt.is_year_end`属性检查给定序列对象的基础数据中的日期是否是一年的最后一天。

```
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series(pd.date_range('2012-12-31 00:00', periods = 5, freq = 'D'))

# Creating the index
idx = ['Day 1', 'Day 2', 'Day 3', 'Day 4', 'Day 5']

# set the index
sr.index = idx

# Print the series
print(sr)
```

**输出:**

![](img/b39d09332de57acef9c1cc2e457692bc.png)

现在我们将使用`Series.dt.is_year_end`属性来检查给定序列对象中的日期是否是一年的最后一天。

```
# check if dates are the
# last day of a year
result = sr.dt.is_year_end

# print the result
print(result)
```

**输出:**

![](img/92480f2bb6e27947bbb859a1b6d7d4a3.png)

正如我们在输出中看到的那样，`Series.dt.is_year_end`属性已经成功访问并返回了指示日期是否是一年的最后一天的布尔值。
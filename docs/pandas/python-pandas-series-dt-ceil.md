# 蟒蛇|熊猫系列. dt.ceil

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-dt-ceil/](https://www.geeksforgeeks.org/python-pandas-series-dt-ceil/)

`Series.dt`可用于访问系列的值，如 datetimelike，并返回几个属性。熊猫 `**Series.dt.ceil()**`功能对指定频率的数据执行上限操作。

> **语法:** Series.dt.ceil(*args，**kwargs)
> 
> **参数:**
> **频率:**将指数提升到的频率水平
> 
> **返回:**日期时间索引、时间增量索引或序列

**示例#1:** 使用`Series.dt.ceil()`函数将给定序列对象的日期时间数据提升到指定的频率。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series(['2012-12-31 08:45', '2019-1-1 12:30', '2008-02-2 10:30',
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

![](img/b894302059abf4db9ded8fe3e0dfccdb.png)

现在我们将使用`Series.dt.ceil()`函数将给定序列对象中的日期时间值上限为每日频率。

```py
# ceil to daily frequency
result = sr.dt.ceil(freq = 'D')

# print the result
print(result)
```

**输出:**

![](img/0abb414b42ecac179434c1d185829c73.png)

正如我们在输出中看到的那样，`Series.dt.ceil()`函数已经成功地将给定序列对象中的日期时间值转换为指定的频率。

**示例#2 :** 使用`Series.dt.ceil()`函数将给定序列对象的日期时间数据提升到指定的频率。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series(pd.date_range('2012-12-31 09:45', periods = 5, freq = 'T',
                            tz = 'Asia / Calcutta'))

# Creating the index
idx = ['Day 1', 'Day 2', 'Day 3', 'Day 4', 'Day 5']

# set the index
sr.index = idx

# Print the series
print(sr)
```

**输出:**

![](img/51ab4112e9736d7032083ecf48b919a1.png)

现在我们将使用`Series.dt.ceil()`函数将给定序列对象中的日期时间值上限为每小时频率。

```py
# ceil to hourly frequency
result = sr.dt.ceil(freq = 'H')

# print the result
print(result)
```

**输出:**

![](img/807758c48e13c498843266d7f36ebc2c.png)

正如我们在输出中看到的那样，`Series.dt.ceil()`函数已经成功地将给定序列对象中的日期时间值转换为指定的频率。
# 蟒蛇|熊猫系列. dt.floor

> 原文:[https://www . geesforgeks . org/python-pandas-series-dt-floor/](https://www.geeksforgeeks.org/python-pandas-series-dt-floor/)

`Series.dt`可用于访问系列的值，如 datetimelike，并返回几个属性。熊猫 `**Series.dt.floor()**`功能对指定频率的数据进行楼层操作。

> **语法:** Series.dt.floor(*args，**kwargs)
> 
> **参数:**
> **频率:**频率等级到楼层指数到
> 
> **返回:**日期时间索引、时间增量索引或序列

**示例#1:** 使用`Series.dt.floor()`函数将给定序列对象的日期时间数据拖到指定的频率。

```
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

现在，我们将使用`Series.dt.floor()`函数将给定序列对象中的日期时间值降至每日频率。

```
# floor to daily frequency
result = sr.dt.floor(freq = 'D')

# print the result
print(result)
```

**输出:**

![](img/cd329015fd268c8bf91a3c311a5a43b4.png)

正如我们在输出中看到的那样，`Series.dt.floor()`函数已经成功地将给定序列对象中的日期时间值钻到了指定的频率。

**示例#2 :** 使用`Series.dt.floor()`函数将给定序列对象的日期时间数据拖到指定的频率。

```
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

现在，我们将使用`Series.dt.floor()`函数将给定序列对象中的日期时间值计算为每小时频率。

```
# floor to hourly frequency
result = sr.dt.floor(freq = 'H')

# print the result
print(result)
```

**输出:**

![](img/098a253626863d830672d5cefe282603.png)

正如我们在输出中看到的那样，`Series.dt.floor()`函数已经成功地将给定序列对象中的日期时间值钻到了指定的频率。
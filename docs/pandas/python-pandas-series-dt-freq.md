# 蟒蛇|熊猫系列. dt.freq

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-dt-freq/](https://www.geeksforgeeks.org/python-pandas-series-dt-freq/)

`Series.dt`可用于访问系列的值，如 datetimelike，并返回几个属性。Pandas `**Series.dt.freq**`属性返回应用于给定序列对象的时间序列频率(如果有)，否则返回 None。

> **语法:** Series.dt.freq
> 
> **参数:**无
> 
> **返回:**频率

**示例#1:** 使用`Series.dt.freq`属性查找给定序列对象中基于日期时间的基础数据的频率。

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

现在我们将使用`Series.dt.freq`属性来查找给定序列对象中基于日期时间的数据的频率。

```
# find the frequency
result = sr.dt.freq

# print the result
print(result)
```

**输出:**

![](img/60b6b3a2b3a346b4225c48e6ce02d530.png)

正如我们在输出中看到的那样，`Series.dt.freq`属性返回了`None`，表示给定日期时间数据的频率未知。

**示例#2 :** 使用`Series.dt.freq`属性查找给定序列对象中基于日期时间的基础数据的频率。

```
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series(pd.date_range('2012-12-31 00:00', periods = 5, freq = 'D',
                            tz = 'US / Central'))

# Creating the index
idx = ['Day 1', 'Day 2', 'Day 3', 'Day 4', 'Day 5']

# set the index
sr.index = idx

# Print the series
print(sr)
```

**输出:**

![](img/b906fe33684d556adb7cbde8289cd8d9.png)

现在我们将使用`Series.dt.freq`属性来查找给定序列对象中基于日期时间的数据的频率。

```
# find the frequency
result = sr.dt.freq

# print the result
print(result)
```

**输出:**

![](img/109b4510871e14b04c2eac1c1364d0f4.png)

正如我们在输出中看到的那样，`Series.dt.freq`属性已经成功地返回了给定 Series 对象中基于基础日期时间的数据的频率。
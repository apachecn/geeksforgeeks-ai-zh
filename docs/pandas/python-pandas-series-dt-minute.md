# 蟒蛇|熊猫系列. dt.minute

> 原文:[https://www . geesforgeks . org/python-pandas-series-dt-minute/](https://www.geeksforgeeks.org/python-pandas-series-dt-minute/)

`Series.dt`可用于访问系列的值，如 datetimelike，并返回几个属性。Pandas `**Series.dt.minute**`属性返回一个 numpy 数组，该数组包含给定序列对象的基础数据中日期时间的分钟数。

> **语法:** Series.dt.minute
> 
> **参数:**无
> 
> **返回:** numpy 数组

**示例#1:** 使用`Series.dt.minute`属性返回给定序列对象的基础数据中日期时间的分钟数。

```
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series(['2012-10-21 09:30', '2019-7-18 12:30', '2008-02-2 10:30',
               '2010-4-22 09:25', '2019-11-8 02:22'])

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

![](img/69f5bc982977eb6e463ef578e21a71f4.png)

现在我们将使用`Series.dt.minute`属性返回给定 Series 对象的基础数据中日期时间的分钟数。

```
# return the minutes
result = sr.dt.minute

# print the result
print(result)
```

**输出:**

![](img/6786e33a4f80ce18c700ce1588d58a11.png)
正如我们在输出中看到的，`Series.dt.minute`属性已经成功访问并返回了给定序列对象的底层数据中的日期时间的分钟数。

**示例 2 :** 使用`Series.dt.minute`属性返回给定 Series 对象的基础数据中日期时间的分钟数。

```
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series(pd.date_range('2012-12-12 12:12',
                       periods = 5, freq = 'H'))

# Creating the index
idx = ['Day 1', 'Day 2', 'Day 3', 'Day 4', 'Day 5']

# set the index
sr.index = idx

# Print the series
print(sr)
```

**输出:**
![](img/908e71bea04cea91346d089922a9b7ca.png)

现在我们将使用`Series.dt.minute`属性返回给定 Series 对象的基础数据中日期时间的分钟数。

```
# return the minutes
result = sr.dt.minute

# print the result
print(result)
```

**输出:**
![](img/4ba5d29c0cd9bd8afb4157326485407b.png)
正如我们在输出中看到的，`Series.dt.minute`属性已经成功访问并返回了给定序列对象的底层数据中的日期时间的分钟数。
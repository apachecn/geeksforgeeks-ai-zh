# 蟒蛇|熊猫系列. asfreq()

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-asfreq/](https://www.geeksforgeeks.org/python-pandas-series-asfreq/)

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

熊猫 `**Series.asfreq()**`功能用于将时间序列转换为指定频率。该功能还提供填充/回填缺失值的填充方法。

> **语法:** Series.asfreq(freq，方法=无，how =无，normalize=False，fill _ value =无)
> 
> **参数:**
> **freq :** DateOffset 对象，或字符串
> **方法:** { '回填'/'填充'/'填充'/'ffill'}，默认值 None
> **how :** 仅针对 PeriodIndex，请参阅 period index . asfreq
> **normalize:**是否将输出索引重置为午夜
> **fill_value :** 用于缺失值的值
> 
> **返回:**已转换:与调用者类型相同

**示例#1:** 使用`Series.asfreq()`功能更改给定序列对象的频率。

```
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series([11, 21, 8, 18, 65, 18, 32, 10, 5, 32, None])

# Create the Index
index_ = pd.date_range('2010-10-09 08:45', periods = 11, freq ='M')

# set the index
sr.index = index_

# Print the series
print(sr)
```

**输出:**

```
2010-12-31 08:45:00     8
2011-01-31 08:45:00    18
2011-02-28 08:45:00    65
2011-03-31 08:45:00    18
2011-04-30 08:45:00    32
2011-05-31 08:45:00    10
2011-06-30 08:45:00     5
2011-07-31 08:45:00    32
2011-08-31 08:45:00   NaN
Freq: M, dtype: float64
```

现在我们使用`Series.asfreq()`功能将给定系列对象的频率改为季度。

```
# change to quarterly frequency
result = sr.asfreq(freq = 'Q')

# Print the result
print(result)
```

**输出:**

```
2010-12-31 08:45:00     8
2011-03-31 08:45:00    18
2011-06-30 08:45:00     5
Freq: Q-DEC, dtype: float64
```

从输出中我们可以看到，`Series.asfreq()`函数已经成功改变了给定序列对象的频率。

**示例 2 :** 使用`Series.asfreq()`功能将给定系列对象的年度频率更改为 3 年的批次。

```
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series([11, 21, 8, 18, 65, 18, 32, 10, 5, 32, None])

# Create the Index
# apply yearly frequency
index_ = pd.date_range('2010-10-09 08:45', periods = 11, freq ='Y')

# set the index
sr.index = index_

# Print the series
print(sr)
```

**输出:**

```
2010-12-31 08:45:00    11.0
2011-12-31 08:45:00    21.0
2012-12-31 08:45:00     8.0
2013-12-31 08:45:00    18.0
2014-12-31 08:45:00    65.0
2015-12-31 08:45:00    18.0
2016-12-31 08:45:00    32.0
2017-12-31 08:45:00    10.0
2018-12-31 08:45:00     5.0
2019-12-31 08:45:00    32.0
2020-12-31 08:45:00     NaN
Freq: A-DEC, dtype: float64
```

现在，我们将使用`Series.asfreq()`功能将给定系列对象的年度频率更改为 3 年的批次。

```
# apply year batch frequency
result = sr.asfreq(freq = '3Y')

# Print the result
print(result)
```

**输出:**

```
2010-12-31 08:45:00    11.0
2013-12-31 08:45:00    18.0
2016-12-31 08:45:00    32.0
2019-12-31 08:45:00    32.0
Freq: 3A-DEC, dtype: float64
```

从输出中我们可以看到，`Series.asfreq()`函数已经成功改变了给定序列对象的频率。
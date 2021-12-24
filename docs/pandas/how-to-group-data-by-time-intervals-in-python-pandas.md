# Python Pandas 中如何按时间间隔对数据进行分组？

> 原文:[https://www . geesforgeks . org/如何按时间间隔分组数据-python-pandas/](https://www.geeksforgeeks.org/how-to-group-data-by-time-intervals-in-python-pandas/)

**先决条件:**T2】熊猫

当您遇到时间序列分析时，按时间间隔对数据进行分组是非常明显的。时间序列是按时间顺序索引(或列出或绘制)的一系列数据点。最常见的是，时间序列是在连续等间隔的时间点上取得的序列。

熊猫提供了两个非常有用的功能，我们可以用它们来对数据进行分组。

*   [重采样()—](https://www.geeksforgeeks.org/python-pandas-dataframe-resample/) 该功能主要用于时间序列数据。这是一种方便的时间序列频率转换和重采样方法。对象必须具有类似日期时间的索引(日期时间索引、周期索引或时间增量索引)，或者将类似日期时间的值传递给 on 或 level 关键字。重采样根据实际数据生成唯一的采样分布。

> ***语法:** DataFrame.resample(规则，how=None，axis=0，fill_method=None，closed=None，label=None，约定='start '，kind=None，loffset=None，limit=None，base=0，on=None，level=None)*
> 
> ***参数:***
> 
> *   ***Rule:** An offset string or object* representing the target conversion.
> *   ***axis:** int, optional, default 0*
> *   ***Closed:** {[right] [left]}*
> *   ***Label:** {[right], [left]}*
> 
> *   ***loffset:** Adjust the time stamp of resampling*
> *   ***base:** For the frequency of even subdivision for one day, the "origin" of the aggregation interval. For example, for the "5 minutes" frequency, the cardinality can be from 0 to 4\. The default is 0\.*
> *   ***on:*** *For a DataFrame, use columns instead of indexes to resample. Columns must be similar to datetime.*
> *   ***Level:*** *For a MultiIndex, the level (name or number) should be used for resampling. The level must be similar to datetime.*

**例:**每月增加的数量，每年增加的总金额。

*   **grouper** -grouper allows users to specify the basis on which users want to analyze data.

> **语法:** dataframe.groupby(pd。Grouper(key，level，freq，axis，sort，label，convention，base，Ioffset，origin，offset))
> 
> **参数:**
> 
> *   **key:** Select the target column to be grouped.
> *   **level:** the level of the target index.
> *   [t0 T0】 freq: group by specify the frequency. If the target column is an object with similar date and time,
> *   T30
> *   **Convention:** If grouper is PeriodIndex and freq parameter is passed,
> *   **base:** only works when freq is passed.
> *   **ioffset:** only works when freq is passed.
> *   **Origin:** Timestamp is based on
> *   **Offset:** The offset time increment is added to the origin 【T60】

### 方法

*   导入模块
*   加载或创建数据
*   根据需要对数据进行重新采样
*   将数据分组

下面给出了使用这种方法的实现:

**使用中的数据帧:** timeseries.csv

**链接:** [此处](https://drive.google.com/file/d/17SU3izLh87rzDwqOOB5KP7H3Z58IsvYU/view?usp=sharing)。

**程序:**使用重采样进行聚合

## **python 3**

```
import numpy as np
import pandas as pd

# loading dataset
data = pd.read_csv('path of dataset')

# setting the index for the data
data = data.set_index(['created_at'])

# converting index to datetime index
data.index = pd.to_datetime(data.index)

# Changing start time for each hour, by default start time is at 0th minute
data.resample('W',  loffset='30Min30s').price.sum().head(2)
data.resample('W', loffset='30Min30s').price.sum().head(2)

# we can also aggregate it will show quantity added in each week
# as well as the total amount added in each week
data.resample('W', loffset='30Min30s').agg(
    {'price': 'sum', 'quantity': 'sum'}).head(5)
```
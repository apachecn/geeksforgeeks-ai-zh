# 熊猫数据框的处理时间

> 原文:[https://www . geesforgeks . org/processing-与熊猫相处的时间-dataframe/](https://www.geeksforgeeks.org/processing-time-with-pandas-dataframe/)

熊猫是根据金融模型创建的，所以正如你所料，它包含了大量的工具来处理日期和时间。有时，我们的数据集中日期和时间的给定格式不能直接用于分析，因此我们预处理这些时间值以获得日期、月份、年份、小时、分钟和秒等特征。
让我们讨论熊猫数据框处理日期和时间的所有不同方法。
**将日期和时间划分为多个特征:**
使用 pd.date_range 创建五个日期和时间，生成固定频率的日期和时间跨度序列。然后我们用熊猫。Series.dt 提取特征。

## 蟒蛇 3

```py
# Load library
import pandas as pd

# calling DataFrame constructor
df = pd.DataFrame()

# Create 6 dates
df['time'] = pd.date_range('2/5/2019', periods = 6, freq ='2H')
print(df['time'])  # print dataframe

# Extract features - year, month, day, hour, and minute
df['year'] = df['time'].dt.year
df['month'] = df['time'].dt.month
df['day'] = df['time'].dt.day
df['hour'] = df['time'].dt.hour
df['minute'] = df['time'].dt.minute

# Show six rows
df.head(6)
```

**输出:**

```py
0   2019-02-05 00:00:00
1   2019-02-05 02:00:00
2   2019-02-05 04:00:00
3   2019-02-05 06:00:00
4   2019-02-05 08:00:00
5   2019-02-05 10:00:00
Name: time, dtype: datetime64[ns]

                time  year  month  day  hour  minute
0 2019-02-05 00:00:00  2019      2    5     0       0
1 2019-02-05 02:00:00  2019      2    5     2       0
2 2019-02-05 04:00:00  2019      2    5     4       0
3 2019-02-05 06:00:00  2019      2    5     6       0
4 2019-02-05 08:00:00  2019      2    5     8       0
5 2019-02-05 10:00:00  2019      2    5    10       0
```

**将字符串转换为时间戳:**
我们使用 pd.to_datetime 将给定的字符串转换为 datetime 格式，然后使用第一种方法从 datetime 中提取不同的特征。

## 蟒蛇 3

```py
# Load libraries
import numpy as np
import pandas as pd

# Create time Strings
dt_strings = np.array(['04-03-2019 12:35 PM',
                       '22-06-2017 11:01 AM',
                       '05-09-2009 07:09 PM'])

# Convert to datetime format
timestamps = [pd.to_datetime(date, format ="%d-%m-%Y%I:%M %p",
                     errors ="coerce") for date in dt_strings]

# Convert to datetimes
timestamps = [pd.to_datetime(date, format ="%d-%m-%Y %I:%M %p",
                      errors ="coerce") for date in dt_strings]
```

**输出:**

> 【时间戳(' 2019-03-04 12:35:00 ')、时间戳(' 2017-06-22 11:01:00 ')、时间戳(' 2009-09-05 19:09:00 ')】

**从给定日期中提取一周中的天数:**
我们使用 Series.dt.weekday_name 从给定日期中查找一周中的一天的名称。

## 蟒蛇 3

```py
# Load library
import pandas as pd
df = pd.DataFrame()

# Create 6 dates
dates = pd.pd.Series(date_range('2/5/2019', periods = 6, freq ='M'))

print(dates)

# Extract days of week and then print
print(dates.dt.weekday_name)
```

**输出:**

```py
0   2019-02-28
1   2019-03-31
2   2019-04-30
3   2019-05-31
4   2019-06-30
5   2019-07-31
dtype: datetime64[ns]
0     Thursday
1       Sunday
2      Tuesday
3       Friday
4       Sunday
5    Wednesday
dtype: object
```

**提取日期和时间范围内的数据:**
我们可以从给定的数据集中获取特定时间范围内的行。
**方法#1:** 如果数据集没有用时间索引。

## 蟒蛇 3

```py
# Load library
import pandas as pd

# Create data frame
df = pd.DataFrame()

# Create datetimes
df['date'] = pd.date_range('1/1/2012', periods = 1000, freq ='H')

print(df.head(5))

# Select observations between two datetimes
x = df[(df['date'] > '2012-1-1 01:00:00') &
       (df['date'] <= '2012-1-1 11:00:00')]

print(x)
```

**输出:**

```py
                 date
0 2012-01-01 00:00:00
1 2012-01-01 01:00:00                // 5 rows of Timestamps out of 1000
2 2012-01-01 02:00:00
3 2012-01-01 03:00:00
4 2012-01-01 04:00:00

                 date
2  2012-01-01 02:00:00
3  2012-01-01 03:00:00
4  2012-01-01 04:00:00
5  2012-01-01 05:00:00               //Timestamps in the given range
6  2012-01-01 06:00:00
7  2012-01-01 07:00:00
8  2012-01-01 08:00:00
9  2012-01-01 09:00:00
10 2012-01-01 10:00:00
11 2012-01-01 11:00:00
```

**方法 2:** 如果数据集是用时间索引的

## 蟒蛇 3

```py
# Load library
import pandas as pd

# Create data frame
df = pd.DataFrame()

# Create datetimes
df['date'] = pd.date_range('1/1/2012', periods = 1000, freq ='H')

# Set index
df = df.set_index(df['date'])

print(df.head(5))

# Select observations between two datetimes
x = df.loc['2012-1-1 04:00:00':'2012-1-1 12:00:00']

print(x)
```

**输出:**

```py
                                   date
date                                   
2012-01-01 00:00:00 2012-01-01 00:00:00
2012-01-01 01:00:00 2012-01-01 01:00:00
2012-01-01 02:00:00 2012-01-01 02:00:00
2012-01-01 03:00:00 2012-01-01 03:00:00                // 5 rows of Timestamps out of 1000
2012-01-01 04:00:00 2012-01-01 04:00:00
                                   date
date                                   
2012-01-01 04:00:00 2012-01-01 04:00:00
2012-01-01 05:00:00 2012-01-01 05:00:00
2012-01-01 06:00:00 2012-01-01 06:00:00
2012-01-01 07:00:00 2012-01-01 07:00:00
2012-01-01 08:00:00 2012-01-01 08:00:00
2012-01-01 09:00:00 2012-01-01 09:00:00               //Timestamps in the given range
2012-01-01 10:00:00 2012-01-01 10:00:00
2012-01-01 11:00:00 2012-01-01 11:00:00
2012-01-01 12:00:00 2012-01-01 12:00:00
```
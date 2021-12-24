# 使用 Python 中的熊猫显示给定年份的所有周日

> 原文:[https://www . geeksforgeeks . org/display-特定年份的所有星期天都在使用蟒蛇皮熊猫/](https://www.geeksforgeeks.org/display-all-the-sundays-of-given-year-using-pandas-in-python/)

让我们看看如何使用熊猫显示一年中的所有星期天。我们将使用`Pandas`模块的`[date_range()](https://www.geeksforgeeks.org/python-pandas-date_range-method/)`功能。

**算法:**

1.  导入`pandas`模块。
2.  使用`date_range()`功能获取所有周日，参数为:
    *   为了显示 2020 年的星期日，`start`参数设置为 2020-01-01。
    *   参数`periods`设置为 52，因为一年大约有 52 周。
    *   参数`freq`设置为 W-SUN，其中 W 指每周，SUN 指周日。
3.  打印取出的`DateTimeIndex`对象。

```
# importing the module
import pandas as pd

# target year
year = "2020"

# instantiating the parameters
start = year + "-01-01"
periods = 52
freq = "W-SUN"

# fetching the Sundays
sundays = pd.date_range(start = start,
                        periods = periods,
                        freq = freq)

# printing the Sundays                        
print(sundays)
```

**输出:**

> 日期时间索引(“2020-01-05”、“2020-01-12”、“2020-01-19”、“2020-01-26”、“2020-02-02”、“2020-02-09”、“2020-02-16”、“2020-02-23”、“2020-t1”、“2020-03-01”、“2020-03-08”、“2020-03-15”、“2020-03-22”、“2020-03-29”、“2020-04-05”、“2020-04-12”)

如果我们想取周日以外的任何一天，我们可以通过将参数`freq`更改为所需的日期来调整上述程序。

```
# importing the module
import pandas as pd

# target year
year = "2020"

# day to be fetched
day = "MON"

# instantiating the parameters
start = year + "-01-01"
periods = 52
freq = "W-" + day

# fetching the days
days = pd.date_range(start = start,
                     periods = periods,
                     freq = freq)

# printing the days                        
print(days)
```

**输出:**

> 日期时间索引(['2020-01-06 '，' 2020-01-13 '，' 2020-01-20 '，' 2020-01-27 '，' t0 ' 2020-02-03 '，' 2020-02-10 '，' 2020-02-17 '，' 2020-02-24 '，' T1 '，' 2020-03-02 '，' 2020-03-09 '，' 2020-03-16 '，' 2020-03-23 '，' 2020-30 '，' 2020-04-06 '，' 2020-04-13 '，'

我们可以将`DateTimeIndex`对象转换为 Series 对象，以获得要提取的日期列表。

```
# importing the module
import pandas as pd

# target year
year = "2020"

# day to be fetched
day = "WED"

# instantiating the parameters
start = year + "-01-01"
periods = 52
freq = "W-" + day

# fetching the days
days = pd.Series(pd.date_range(start = start,
                               periods = periods,
                               freq = freq))

# printing the days                        
print(days)
```

**输出:**

```
0    2020-01-01
1    2020-01-08
2    2020-01-15
3    2020-01-22
4    2020-01-29
5    2020-02-05
6    2020-02-12
7    2020-02-19
8    2020-02-26
9    2020-03-04
10   2020-03-11
11   2020-03-18
12   2020-03-25
13   2020-04-01
14   2020-04-08
15   2020-04-15
16   2020-04-22
17   2020-04-29
18   2020-05-06
19   2020-05-13
20   2020-05-20
21   2020-05-27
22   2020-06-03
23   2020-06-10
24   2020-06-17
25   2020-06-24
26   2020-07-01
27   2020-07-08
28   2020-07-15
29   2020-07-22
30   2020-07-29
31   2020-08-05
32   2020-08-12
33   2020-08-19
34   2020-08-26
35   2020-09-02
36   2020-09-09
37   2020-09-16
38   2020-09-23
39   2020-09-30
40   2020-10-07
41   2020-10-14
42   2020-10-21
43   2020-10-28
44   2020-11-04
45   2020-11-11
46   2020-11-18
47   2020-11-25
48   2020-12-02
49   2020-12-09
50   2020-12-16
51   2020-12-23
dtype: datetime64[ns]
```
# 创建熊猫时间序列以显示给定年份的所有周日

> 原文:[https://www . geesforgeks . org/create-a-pandas-time series-to-display-特定年份的所有星期日/](https://www.geeksforgeeks.org/create-a-pandas-timeseries-to-display-all-the-sundays-of-given-year/)

假设我们需要找出 2020 年所有的星期天。然后我们使用熊猫模块。如果我们需要找到显示所有周日的时间序列，我们使用 **panda。Series()** 类，它是一个一维标记数组，能够保存任何数据。

> **语法:**熊猫。系列(*数据=无*，*索引=无*，*数据类型=无*，*名称=无*，*副本=假*，*快速路径=假*)
> 
> **返回:**系列对象

想了解更多熊猫系列[点击这里](https://www.geeksforgeeks.org/python-pandas-series/)。

另外，我们使用 panda 的 **data_range()** 函数来指定我们的确切需求。此方法用作返回固定频率日期时间索引的常规函数。

> **语法:**pandas . date _ range(start = None，end=None，periods=None，freq=None，tz=None，normalize=False，name=None，closed=None，**kwargs)
> 
> **返回:**返回固定频率的日期时间索引。

要深入了解 data_range()函数[，请单击此处。](https://www.geeksforgeeks.org/python-pandas-date_range-method/)

现在，我们来看节目。

**代码:**

## 蟒蛇 3

```py
# import pandas library
import pandas as pd

# create s series of all sundays
result = pd.Series(pd.date_range('2020-01-01',
                                 periods = 52, 
                                 freq = 'W-SUN'))
print("All Sundays in 2020:")

# show the series
print(result)
```

**输出:**

```py
All Sundays in 2020:
0    2020-01-05
1    2020-01-12
2    2020-01-19
3    2020-01-26
4    2020-02-02
5    2020-02-09
6    2020-02-16
7    2020-02-23
8    2020-03-01
9    2020-03-08
10   2020-03-15
11   2020-03-22
12   2020-03-29
13   2020-04-05
14   2020-04-12
15   2020-04-19
16   2020-04-26
17   2020-05-03
18   2020-05-10
19   2020-05-17
20   2020-05-24
21   2020-05-31
22   2020-06-07
23   2020-06-14
24   2020-06-21
25   2020-06-28
26   2020-07-05
27   2020-07-12
28   2020-07-19
29   2020-07-26
30   2020-08-02
31   2020-08-09
32   2020-08-16
33   2020-08-23
34   2020-08-30
35   2020-09-06
36   2020-09-13
37   2020-09-20
38   2020-09-27
39   2020-10-04
40   2020-10-11
41   2020-10-18
42   2020-10-25
43   2020-11-01
44   2020-11-08
45   2020-11-15
46   2020-11-22
47   2020-11-29
48   2020-12-06
49   2020-12-13
50   2020-12-20
51   2020-12-27
dtype: datetime64[ns]

```
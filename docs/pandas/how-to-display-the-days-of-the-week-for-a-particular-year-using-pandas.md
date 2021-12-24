# 如何使用熊猫显示特定年份的星期几？

> 原文:[https://www . geeksforgeeks . org/如何显示特定年份使用熊猫的星期几/](https://www.geeksforgeeks.org/how-to-display-the-days-of-the-week-for-a-particular-year-using-pandas/)

给定日期和年份。任务是显示一年中一周的所有日子。可以使用[**pandas . date _ range()**](https://www.geeksforgeeks.org/python-pandas-date_range-method/)**功能找到。该函数用于获取固定频率的日期时间索引。**

> ****语法:**pandas . date _ range(start = None，end=None，periods=None，freq=None，tz=None，normalize=False，name=None，closed=None，**kwargs)**

****进场:****

*   **进口熊猫模块**
*   **创建用于计算时间序列的参数函数。**
*   **使用 pandas.date_range()函数生成固定频率的日期序列**
*   **存储到熊猫系列内的功能**
*   **并返回全天的日期**

****下面是实现。****

 **## 蟒 3

```py
# importing module
import pandas as pd

# User define function
def Time_series(day, yy):
    date_range = pd.date_range(yy+'-01-01', periods=52, freq=day)
    result = pd.Series(date_range)
    print(f"All { day[2:] } in " + yy + ":")
    print(result)

# Input from user
day = "wed"
yy = "2020"

# Check the day form input variable
if day == 'monday' or day == 'mon':
    Time_series('W-mon', yy)
elif day == 'tuesday' or day == 'tue':
    Time_series('W-tue', yy)
elif day == 'wednesday' or day == 'wed':
    Time_series('W-wed', yy)
elif day == 'thursday' or day == 'thu':
    Time_series('W-thu', yy)
elif day == 'friday' or day == 'fri':
    Time_series('W-fri', yy)
elif day == 'saturday' or day == 'sat':
    Time_series('W-fri', yy)
else:
    Time_series('W-sun', yy)
```** 

****输出:****

```py
All wed in 2020:
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

****注意:**周期 52 因为一年的总天数是 365，那么每天会重复 52 次(365/7=52)。**
# 使用 NumPy

获取昨天、今天和明天的日期

> 原文:[https://www . geeksforgeeks . org/get-date-of-of-day-today-to-day-use-numpy/](https://www.geeksforgeeks.org/get-the-dates-of-yesterday-today-and-tomorrow-using-numpy/)

在 NumPy 中，借助于 NumPy.datetime64('today '，' D ')，我们将找到今天的日期，如果我们想要今天之前的某个日期，那么我们将借助于 np.timedelta64()从今天减去无日期。如果我们想要今天之后的某个日期，那么我们将在 np.timedelta64()的帮助下从今天开始添加日期编号。
对于昨天，我们将减去 1 个日期，对于明天，我们将增加 1 个日期。

**示例#1:** 获取昨天、今天和明天的日期。

## 蟒蛇 3

```py
import numpy as np

# for today
today = np.datetime64('today', 'D')
print("Today: ", today)

# for yesterday
yesterday = np.datetime64('today', 'D')
- np.timedelta64(1, 'D')

print("Yestraday: ", yesterday)

# for tomorrow
tomorrow = np.datetime64('today', 'D')
+ np.timedelta64(1, 'D')

print("Tomorrow: ", tomorrow)
```
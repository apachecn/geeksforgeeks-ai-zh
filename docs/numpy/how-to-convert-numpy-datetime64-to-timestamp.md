# 如何将 NumPy datetime64 转换为 Timestamp？

> 原文:[https://www . geesforgeks . org/how-convert-numpy-datetime 64-to-timestamp/](https://www.geeksforgeeks.org/how-to-convert-numpy-datetime64-to-timestamp/)

在本文中，我们将讨论如何将 NumPy datetime64 转换为 Timestamp。为了更好地理解，首先让我们看下面的例子:

```
If the current datetime64 is as follows: 2020-08-18 09:31:51.944622
then,
the required timestamp in seconds will be: 1597743111.944622
the required timestamp in minutes will be: 26629051.8657437
the required timestamp in an hour will be: 443817.53109572834

```

**进场:**

*   取日期通过[**np.datetime64()。**](https://www.geeksforgeeks.org/python-numpy-datetime64-method/)
*   从默认系统日期 1970-01-01T00:00:00Z 中减去该日期。
*   借助 **np.timedelta64()** 将日期转换为秒、分、小时。

**例 1:**

## 蟒蛇 3

```
# importing required library
import numpy as np
from datetime import datetime

# extracting current date 
# in utc format
date = datetime.utcnow()

print("Printing the Current date:",
      date)

# converting the current date
# in datetime64 format
date64 = np.datetime64(date)

# converting date time into second timestamp 
ts = (date64 - np.datetime64('1970-01-01T00:00:00Z')) / np.timedelta64(1, 's')

print("Printing the converted datetime in Timestamp in seconds:",
     ts)

# converting date time into minute timestamp 
tm = (date64 - np.datetime64('1970-01-01T00:00:00Z')) / np.timedelta64(1, 'm')

print("Printing the converted datetime in Timestamp in minutes:",
     ts)

# converting date time into hour timestamp 
th = (date64 - np.datetime64('1970-01-01T00:00:00Z')) / np.timedelta64(1, 'h')

print("Printing the converted datetime in Timestamp in hour:",
      th)
```

**输出:**

> 打印当前日期:2020-08-26 10:07:54.820878
> 以秒为单位打印转换后的日期时间以时间戳为单位:1598436474.820878
> 以分钟为单位打印转换后的日期时间以时间戳为单位:1598436474.820878
> 以小时为单位打印转换后的日期时间以时间戳为单位:44401.0000800088

**示例 2:** 转换 2020 年 8 月 15 日的秒、分、小时时间戳:

## 蟒蛇 3

```
#importing required library
import numpy as np
from datetime import datetime

print("Printing the date:")

# extracting current date in utc format
dt64 = np.datetime64('2020-08-15');

print(dt64)

# converting date time into second timestamp 
ts = (dt64 - np.datetime64('1970-01-01T00:00:00Z')) / np.timedelta64(1, 's')
print("Printing the converted datetime in Timestamp in seconds:", 
      ts)
print("Printing the converted datetime in Timestamp in minutes")

# converting date time into minute timestamp 
tm = (dt64 - np.datetime64('1970-01-01T00:00:00Z')) / np.timedelta64(1, 'm')
print(tm)

print("Printing the converted datetime in Timestamp in hour")

# converting date time into hour timestamp 
th = (dt64 - np.datetime64('1970-01-01T00:00:00Z')) / np.timedelta64(1, 'h')
print(th)
```

**输出:**

> 打印日期:
> 2020-08-15
> 以秒为单位打印转换后的时间戳日期时间:
> 1597449600.0
> 以分钟为单位打印转换后的时间戳日期时间
> 26624160.0
> 以小时为单位打印转换后的时间戳日期时间
> 443736.0
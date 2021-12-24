# Python |熊猫时间戳。timetz

> 原文:[https://www . geesforgeks . org/python-pandas-timestamp-timetz/](https://www.geeksforgeeks.org/python-pandas-timestamp-timetz/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

Pandas `**Timestamp.timetz()**`函数返回时间对象，其时间和 tzinfo 与给定的 Timestamp 对象相同。

> **语法:** Timestamp.timetz()
> 
> **参数:**无
> 
> **返回:**时间对象

**示例#1:** 使用`Timestamp.timetz()`函数返回包含给定时间戳对象的时间和时区信息的时间对象。

```py
# importing pandas as pd
import pandas as pd

# Create the Timestamp object
ts = pd.Timestamp(year = 2011,  month = 11, day = 21, 
                  hour = 10, second = 49, tz = 'US/Central') 

# Print the Timestamp object
print(ts)
```

**输出:**

![](img/46bacf48d4678c79bc6cd69f1866e796.png)

现在我们将使用`Timestamp.timetz()`函数来查找给定时间戳的时间和时区信息。

```py
# return time object
ts.timetz()
```

**输出:**

![](img/ad09548c9cac38e94bf0799b2ecc03e5.png)

正如我们在输出中看到的那样，`Timestamp.timetz()`函数返回了一个包含给定时间戳的时间和时区信息的时间对象。

**示例#2:** 使用`Timestamp.timetz()`函数返回包含给定时间戳对象的时间和时区信息的时间对象。

```py
# importing pandas as pd
import pandas as pd

# Create the Timestamp object
ts = pd.Timestamp(year = 2009, month = 5, day = 31, 
                  hour = 4, second = 49, tz = 'Europe/Berlin')

# Print the Timestamp object
print(ts)
```

**输出:**

![](img/d98f3b94a4739afa3c5c3e1b0193125e.png)

现在我们将使用`Timestamp.timetz()`函数来查找给定时间戳的时间和时区信息。

```py
# return time object
ts.timetz()
```

**输出:**

![](img/2050c39a29cbf16b1af98d4724a3cc7b.png)

正如我们在输出中看到的那样，`Timestamp.timetz()`函数返回了一个包含给定时间戳的时间和时区信息的时间对象。
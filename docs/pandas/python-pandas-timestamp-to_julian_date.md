# Python | Pandas timestamp . to _ Julian _ date

> 原文:[https://www . geesforgeks . org/python-pandas-timestamp-to _ Julian _ date/](https://www.geeksforgeeks.org/python-pandas-timestamp-to_julian_date/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**Timestamp.to_julian_date()**`函数将给定的时间戳转换为儒略日。儒略日 0 的值是公元前 4713 年 1 月 1 日中午。

> **语法:** Timestamp.to_julian_date()
> 
> **参数:**无
> 
> **返回:**儒略日

**示例#1:** 使用`Timestamp.to_julian_date()`函数将给定的时间戳转换为儒略日。

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

现在我们将使用`Timestamp.to_julian_date()`函数将给定的时间戳转换为儒略日。

```py
# convert to julian date
ts.to_julian_date()
```

**输出:**

![](img/e0e3c506bd6011af2138b9f251b07ba7.png)

正如我们在输出中看到的那样，`Timestamp.to_julian_date()`函数已经将给定的时间戳转换为儒略日。

**示例 2:** 使用`Timestamp.to_julian_date()`函数将给定的时间戳转换为儒略日。

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

现在我们将使用`Timestamp.to_julian_date()`函数将给定的时间戳转换为儒略日。

```py
# convert to julian date
ts.to_julian_date()
```

**输出:**

![](img/61c23a5efb6ba5dc08d51259d8c22484.png)

正如我们在输出中看到的那样，`Timestamp.to_julian_date()`函数已经将给定的时间戳转换为儒略日。
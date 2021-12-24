# Python | Pandas timestamp . isoweekday

> 原文:[https://www . geesforgeks . org/python-pandas-timestamp-isoweekday/](https://www.geeksforgeeks.org/python-pandas-timestamp-isoweekday/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**Timestamp.isoweekday()**`功能返回日期代表的星期几。其中一周的天数从周一的 1 到周日的 7。

> **语法:** Timestamp.isoweekday()
> 
> **参数:**无
> 
> **返回:**工作日

**示例#1:** 使用`Timestamp.isoweekday()`函数在给定的 Timestamp 对象中查找日期的星期几。

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

![](img/ee694c9af88333eeafa810576fa77c25.png)

现在我们将使用`Timestamp.isoweekday()`函数在 ts 对象中查找日期的星期几。

```py
# return the day of the week
ts.isoweekday()
```

**输出:**

![](img/020104c28ddc900a14a2c295373f2590.png)

正如我们在输出中看到的那样，`Timestamp.isoweekday()`函数返回了 1，表示给定 Timestamp 对象中的日期是星期一。

**示例 2:** 使用`Timestamp.isoweekday()`函数在给定的时间戳对象中查找日期的星期几。

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

![](img/e2c4d93f6eeb606ab122d97734870a13.png)

现在我们将使用`Timestamp.isoweekday()`函数在 ts 对象中查找日期的星期几。

```py
# return the day of the week
ts.isoweekday()
```

**输出:**

![](img/184e1779e030f8db27abd2dc9a57a56a.png)

我们可以在输出中看到，`Timestamp.isoweekday()`函数返回了 7，表示给定 Timestamp 对象中的日期是星期日。
# Python | Pandas timestamp . dayofweek

> 原文:[https://www . geesforgeks . org/python-pandas-timestamp-dayofweek/](https://www.geeksforgeeks.org/python-pandas-timestamp-dayofweek/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**Timestamp.dayofweek**`属性返回给定时间戳对象中一周中某一天的值。日期从 0 到 6，其中 0 是星期一，6 是星期日。

> **语法:** Timestamp.dayofweek
> 
> **参数:**无
> 
> **返回:**星期几

**示例#1:** 使用`Timestamp.dayofweek`属性在给定的 Timestamp 对象中查找星期几。

```py
# importing pandas as pd
import pandas as pd

# Create the Timestamp object
ts = pd.Timestamp(2017, 1, 15, 12)

# Print the Timestamp object
print(ts)
```

**输出:**

![](img/ffd6ae50d6cf4625e1be839ecc51b75e.png)

现在我们将使用`Timestamp.dayofweek`属性找出给定时间戳对象中的星期几。

```py
# return day of the week
ts.dayofweek
```

**输出:**

![](img/a0e977ddcb25ab7dd02fe6e867023a12.png)

正如我们在输出中看到的那样，`Timestamp.dayofweek`属性返回了 6，表示它是给定 Timestamp 对象中一周的最后一天。

**示例 2:** 使用`Timestamp.dayofweek`属性在给定的时间戳对象中查找一周中的某一天。

```py
# importing pandas as pd
import pandas as pd

# Create the Timestamp object
ts = pd.Timestamp(year = 2009, month = 10, 
          day = 21, tz = 'Europe/Berlin')

# Print the Timestamp object
print(ts)
```

**输出:**

![](img/5c9ffc3eb01058bce36e942e0e923bdb.png)

现在我们将使用`Timestamp.dayofweek`属性找出给定时间戳对象中的星期几。

```py
# return day of the week
ts.dayofweek
```

**输出:**

![](img/e5c545886e28caaa277be4a3418c508d.png)

正如我们在输出中看到的那样，`Timestamp.dayofweek`属性返回了 2，表示 Timestamp 对象中给定的日期是星期三。
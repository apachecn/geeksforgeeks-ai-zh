# Python | Pandas datetime index . is _ month _ end

> 原文:[https://www . geesforgeks . org/python-pandas-datetime index-is _ month _ end/](https://www.geeksforgeeks.org/python-pandas-datetimeindex-is_month_end/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

Pandas `**DatetimeIndex.is_month_end**`属性返回一个 numpy 数组，该数组包含与 DatetimeIndex 对象中的每个条目相对应的逻辑值。如果日期是一个月的最后一天，则该值设置为`True`。否则该函数返回`False`，表示日期不是一个月的最后一天。

> **语法:** DatetimeIndex.is_month_end
> 
> **返回:**包含逻辑值的 numpy 数组。

**示例#1:** 使用`DatetimeIndex.is_month_end`属性检查 DatetimeIndex 对象中的日期是否是一个月的最后一天。

```py
# importing pandas as pd
import pandas as pd

# Create the DatetimeIndex
didx = pd.DatetimeIndex(['2014-01-31', '2014-02-28', 
                         '2015-04-01', '2000-12-02'])

# Print the DatetimeIndex
print(didx)
```

**输出:**
![](img/a3b5443a7c107b77327e1bf9b9e24156.png)

现在我们想知道给定的 DatetimeIndex 对象中包含的日期是否是一个月的最后一天。

```py
# find if the days are the last day of the month.
didx.is_month_end
```

**输出:**
![](img/aafd89f201e6df8321ba98ecfed4c123.png)
正如我们在输出中看到的，该函数返回了一个 numpy 数组，其中包含 DatetimeIndex 对象的每个条目的逻辑值。`True`值表示对应日期是当月的最后一天，`False`值表示对应日期不是当月的最后一天。

**示例#2:** 使用`DatetimeIndex.is_month_end`属性检查 DatetimeIndex 对象中出现的日期是否是一个月的最后一天。

```py
# importing pandas as pd
import pandas as pd

# Create the DatetimeIndex
didx = pd.DatetimeIndex(start ='2000-01-31 06:30', freq ='BM', 
                             periods = 5, tz ='Asia/Calcutta')

# Print the DatetimeIndex
print(didx)
```

**输出:**
![](img/f94038d20d1199e0f5994271c3fd5203.png)

现在我们想知道给定的 DatetimeIndex 对象中包含的日期是否是一个月的最后一天。

```py
# find if the days are the last day of the month.
didx.is_month_end
```

**输出:**
![](img/0187cbd6ea6824dc3aeeb61b9140e9a9.png)
正如我们在输出中看到的，该函数返回了一个 numpy 数组，其中包含 DatetimeIndex 对象的每个条目的逻辑值。`True`值表示对应日期是当月的最后一天，`False`值表示对应日期不是当月的最后一天。
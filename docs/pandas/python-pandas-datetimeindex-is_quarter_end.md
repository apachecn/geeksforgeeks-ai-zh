# Python | Pandas datetime index . is _ quarter _ end

> 原文:[https://www . geesforgeks . org/python-pandas-datetime index-is _ quarter _ end/](https://www.geeksforgeeks.org/python-pandas-datetimeindex-is_quarter_end/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**DatetimeIndex.is_quarter_end**`属性是日期是否是一个季度的最后一天的指标。如果日期是本季度的最后一天，则返回`True`，否则返回`False`。

> **语法:**datetime index . is _ quarter _ end
> 
> **返回:**包含逻辑值的 numpy 数组。

**示例#1:** 使用`DatetimeIndex.is_quarter_end`属性检查 DatetimeIndex 对象中出现的日期是否是季度的最后一天。

```py
# importing pandas as pd
import pandas as pd

# Create the DatetimeIndex
didx = pd.DatetimeIndex(['2014-01-31', '2014-04-30', '2017-03-31', '2000-12-02'])

# Print the DatetimeIndex
print(didx)
```

**输出:**
![](img/a183d18f5be7cd8cfd000a33f571a194.png)

现在我们想知道给定 DatetimeIndex 对象中包含的日期是否是季度的最后一天。

```py
# find if the days are the last day of the quarter.
didx.is_quarter_end
```

**输出:**
![](img/6fd065529430b377ac2cc93fc27bbc78.png)
正如我们在输出中看到的，该函数返回了一个 numpy 数组，其中包含 DatetimeIndex 对象的每个条目的逻辑值。`True`值表示对应日期是季度的最后一天，`False`值表示对应日期不是季度的最后一天。

**示例#2:** 使用`DatetimeIndex.is_quarter_end`属性检查 DatetimeIndex 对象中出现的日期是否是季度的最后一天。

```py
# importing pandas as pd
import pandas as pd

# Create the DatetimeIndex
idx = pd.date_range('2011-03-30', periods = 5)

# Print the DatetimeIndex
print(didx)
```

**输出:**
![](img/9905f85872d7b7464bd534b3f4db326c.png)

现在我们想知道给定 DatetimeIndex 对象中包含的日期是否是季度的最后一天。

```py
# find if the days are the last day of the quarter.
didx.is_quarter_end
```

**输出:**
![](img/e68ea8d5761f011193455b316b0e45c9.png)
正如我们在输出中看到的，该函数返回了一个 numpy 数组，其中包含 DatetimeIndex 对象的每个条目的逻辑值。`True`值表示对应日期是季度的最后一天，`False`值表示对应日期不是季度的最后一天。
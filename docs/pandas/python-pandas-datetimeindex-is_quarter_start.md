# Python | Pandas datetime index . is _ quarter _ start

> 原文:[https://www . geesforgeks . org/python-pandas-datetime index-is _ quarter _ start/](https://www.geeksforgeeks.org/python-pandas-datetimeindex-is_quarter_start/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**DatetimeIndex.is_quarter_start**`属性是日期是否是一个季度的第一天的指标。如果日期是本季度的第一天，则返回`True`，否则返回`False`。

> **语法:**datetime index . is _ quarter _ start
> 
> **返回:**包含逻辑值的 numpy 数组。

**示例#1:** 使用`DatetimeIndex.is_quarter_start`属性检查 DatetimeIndex 对象中出现的日期是否是季度的第一天。

```
# importing pandas as pd
import pandas as pd

# Create the DatetimeIndex
didx = pd.DatetimeIndex(['2014-01-31', '2014-04-1', '2015-08-01', '2000-12-02'])

# Print the DatetimeIndex
print(didx)
```

**输出:**
![](img/c427c588f5751a9bad7d6136bd244df8.png)

现在我们想知道给定 DatetimeIndex 对象中包含的日期是否是季度的第一天。

```
# find if the days are the first day of the quarter.
didx.is_quarter_start
```

**输出:**
![](img/a57bc3f63efb9f94a7af49b26713e3d4.png)
正如我们在输出中看到的，该函数返回了一个 numpy 数组，其中包含 DatetimeIndex 对象的每个条目的逻辑值。`True`值表示对应日期是季度的第一天，`False`值表示对应日期不是季度的第一天。

**示例#2:** 使用`DatetimeIndex.is_quarter_start`属性检查 DatetimeIndex 对象中显示的日期是否是季度的第一天。

```
# importing pandas as pd
import pandas as pd

# Create the DatetimeIndex
didx = pd.date_range('2011-03-30', periods = 5)

# Print the DatetimeIndex
print(didx)
```

**输出:**
![](img/a9a327cf36006440d6fefe69c59efde6.png)

现在我们想知道给定 DatetimeIndex 对象中包含的日期是否是季度的第一天。

```
# find if the days are the first day of the quarter.
didx.is_quarter_start
```

**输出:**
![](img/0e068974702618441686e2d7b029f101.png)
正如我们在输出中看到的，该函数返回了一个包含 DatetimeIndex 对象的每个条目的逻辑值的 *numpy* 数组。`True`值表示对应日期是季度的第一天，`False`值表示对应日期不是季度的第一天。
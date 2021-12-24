# Python | Pandas datetime index . is _ year _ start

> 原文:[https://www . geesforgeks . org/python-pandas-datetime index-is _ year _ start/](https://www.geeksforgeeks.org/python-pandas-datetimeindex-is_year_start/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**DatetimeIndex.is_year_start**`属性是日期是否是一年的第一天的指标。如果日期是一年的第一天，它会返回`True`，否则会返回`False`。

> **语法:** DatetimeIndex.is_year_start
> 
> **返回:**包含逻辑值的 numpy 数组。

**示例#1:** 使用`DatetimeIndex.is_year_start`属性检查 DatetimeIndex 对象中的日期是否是一年中的第一天。

```py
# importing pandas as pd
import pandas as pd

# Create the DatetimeIndex
didx = pd.DatetimeIndex(['2014-01-01', '2014-04-30', '2017-03-31', '2000-12-02'])

# Print the DatetimeIndex
print(didx)
```

**输出:**
![](img/649200df1c5a4e1f744a6f797c802762.png)

现在我们想知道给定 DatetimeIndex 对象中包含的日期是否是一年中的第一天。

```py
# find if the days are the first day of the year.
didx.is_year_start
```

**输出:**
![](img/c2faf9bed87f06662b6da99ba5202106.png)
正如我们在输出中看到的，该函数返回了一个 numpy 数组，其中包含 DatetimeIndex 对象的每个条目的逻辑值。`True`值表示对应日期是一年的第一天，`False`值表示对应日期不是一年的第一天。

**示例#2:** 使用`DatetimeIndex.is_year_start`属性检查 DatetimeIndex 对象中的日期是否是一年中的第一天。

```py
# importing pandas as pd
import pandas as pd

# Create the DatetimeIndex
didx = pd.date_range('2011-12-30', periods = 5)

# Print the DatetimeIndex
print(didx)
```

**输出:**
![](img/37f1363bf03197a0cea9853300f4ecf4.png)

现在我们想知道给定 DatetimeIndex 对象中包含的日期是否是一年中的第一天。

```py
# find if the days are the first day of the year.
didx.is_year_start
```

**输出:**
![](img/1875ba934bf1c40a5689e623303f7c0d.png)

正如我们在输出中看到的，该函数返回了一个 numpy 数组，其中包含 DatetimeIndex 对象的每个条目的逻辑值。`True`值表示对应日期是一年的第一天，`False`值表示对应日期不是一年的第一天。
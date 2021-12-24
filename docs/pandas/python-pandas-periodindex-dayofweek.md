# 蟒蛇|熊猫 PeriodIndex.dayofweek

> 原文:[https://www . geesforgeks . org/python-pandas-period index-dayofweek/](https://www.geeksforgeeks.org/python-pandas-periodindex-dayofweek/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

pandas**PeriodIndex . dayofweek**属性返回一个 Index 对象，该对象包含给定 period Index 对象中每个元素的星期值。“0”是一周的第一天，“6”是一周的最后一天。

> **语法:**period Index . day fweek
> T3】参数:None
> T6】返回: Index

**示例#1:** 使用 PeriodIndex.dayofweek 属性查找给定 PeriodIndex 对象中每个元素的星期值。

## 蟒蛇 3

```py
# importing pandas as pd
import pandas as pd

# Create the PeriodIndex object
pidx = pd.PeriodIndex(start ='2005-12-21',
             end ='2005-12-29', freq ='D')

# Print the PeriodIndex object
print(pidx)
```

**输出:**

![](img/6fc69b6619a8ec8017757a90de497b6c.png)

现在，我们将使用 PeriodIndex.dayofweek 属性来查找给定对象中每个元素的星期值。

## 蟒蛇 3

```py
# return the value of days of the week
pidx.dayofweek
```

**输出:**

![](img/0bb701e0941b266c70bca651b9294166.png)

正如我们在输出中看到的，PeriodIndex.dayofweek 属性返回了一个 Index 对象，该对象包含给定 PeriodIndex 对象中每个元素的星期值。

**示例#2:** 使用 PeriodIndex.dayofweek 属性查找给定 PeriodIndex 对象中每个元素的星期值。

## 蟒蛇 3

```py
# importing pandas as pd
import pandas as pd

# Create the PeriodIndex object
pidx = pd.PeriodIndex(start ='2011-03-14 ',
              end ='2011-03-21', freq ='D')

# Print the PeriodIndex object
print(pidx)
```

**输出:**

![](img/f985d87b118964afe248966d74311800.png)

现在，我们将使用 PeriodIndex.dayofweek 属性来查找给定对象中每个元素的星期值。

## 蟒蛇 3

```py
# return the value of days of the week
pidx.dayofweek
```

**输出:**

![](img/ecfcbc1a636a2c31a2785dd2969b6349.png)

正如我们在输出中看到的，PeriodIndex.dayofweek 属性返回了一个 Index 对象，该对象包含给定 PeriodIndex 对象中每个元素的星期值。
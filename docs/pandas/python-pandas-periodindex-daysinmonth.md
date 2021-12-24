# 蟒蛇|熊猫 PeriodIndex.daysinmonth

> 原文:[https://www . geesforgeks . org/python-pandas-period index-days in month/](https://www.geeksforgeeks.org/python-pandas-periodindex-daysinmonth/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 **PeriodIndex.daysinmonth** 属性返回一个 Index 对象。索引包含给定周期索引对象中每个元素在一个月中的天数。

> **语法:**period Index . daysinmonth
> T3】参数:None
> T6】返回: Index

**示例#1:** 使用 PeriodIndex.daysinmonth 属性查找给定 PeriodIndex 对象中每个元素的月天数。

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

现在，我们将使用 PeriodIndex.daysinmonth 属性来查找给定对象中每个元素在一个月中的天数。

## 蟒蛇 3

```py
# return the number of days in month
pidx.daysinmonth
```

**输出:**

![](img/df61a0dd8a89ef4aaab1fa660236a336.png)

正如我们在输出中看到的，PeriodIndex.daysinmonth 属性返回了一个 Index 对象，该对象包含给定 PeriodIndex 对象中每个元素的月天数。

**示例#2:** 使用 PeriodIndex.daysinmonth 属性查找给定 PeriodIndex 对象中每个元素的月天数。

## 蟒蛇 3

```py
# importing pandas as pd
import pandas as pd

# Create the PeriodIndex object
pidx = pd.PeriodIndex(start ='2011-02-14 ',
              end ='2011-02-21', freq ='D')

# Print the PeriodIndex object
print(pidx)
```

**输出:**

![](img/a5f5dd270d5cc6838dcfebc3b79b296c.png)

现在，我们将使用 PeriodIndex.daysinmonth 属性来查找给定对象中每个元素在一个月中的天数。

## 蟒蛇 3

```py
# return the number of days in month
pidx.daysinmonth
```

**输出:**

![](img/939e223fde6c6e0569b6aa59ce6ffce9.png)

正如我们在输出中看到的，PeriodIndex.daysinmonth 属性返回了一个 Index 对象，该对象包含给定 PeriodIndex 对象中每个元素的月天数。
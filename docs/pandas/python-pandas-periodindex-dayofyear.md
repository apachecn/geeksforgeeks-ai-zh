# 蟒蛇|熊猫 period index . day fyear

> 原文:[https://www . geesforgeks . org/python-pandas-period index-dayofyear/](https://www.geeksforgeeks.org/python-pandas-periodindex-dayofyear/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫**period Index . day fyear**属性返回一个 Index 对象。索引包含给定周期索引对象中每个元素每年的第几天。

> **语法:**period Index . day fyear
> T3】参数:None
> T6】返回: Index

**示例#1:** 使用 PeriodIndex . day fyear 属性查找给定 period index 对象中每个元素的年序数的值。

## 蟒蛇 3

```
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

现在我们将使用 period index . day fyear 属性为给定对象中的每个元素查找一年中的第几天的值。

## 蟒蛇 3

```
# return the value of ordinal
# days of the year
pidx.dayofyear
```

**输出:**

![](img/e0bfd5fa6943a46386adec327c58db0c.png)

正如我们在输出中看到的，PeriodIndex . day fyear 属性返回了一个 Index 对象，该对象包含给定 period Index 对象中每个元素的年序数。

**示例#2:** 使用 PeriodIndex . day fyear 属性查找给定 period index 对象中每个元素的年序数的值。

## 蟒蛇 3

```
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

现在我们将使用 period index . day fyear 属性为给定对象中的每个元素查找一年中的第几天的值。

## 蟒蛇 3

```
# return the value of ordinal
# days of the year
pidx.dayofyear
```

**输出:**

![](img/12deffde981eccb8a03cea775d0f92d6.png)

正如我们在输出中看到的，PeriodIndex . day fyear 属性返回了一个 Index 对象，该对象包含给定 period Index 对象中每个元素的年序数。
# 如何用熊猫的频率确定周期范围？

> 原文:[https://www . geeksforgeeks . org/如何用熊猫频率确定周期范围/](https://www.geeksforgeeks.org/how-to-determine-period-range-with-frequency-in-pandas/)

在熊猫中，我们可以借助 period_range()来确定带有频率的周期范围。**pandas . period _ range()**是 Pandas 中的通用函数之一，用于返回固定频率的 PeriodIndex，默认频率为日(日历)。

> ***语法:** pandas.to_numeric(arg，errors='raise '，downcast=None)*
> 
> ***参数:***
> ***开始:**左界为生成期间*
> ***结束:**右界为生成期间*
> ***期间:**要生成的期间数*
> ***freq :** 频率别名*
> **名称:**生成的期间索引的名称
> 
> ***返回:**周期指数*

**例 1:**

## 蟒蛇 3

```py
import pandas as pd

# initialize country
country = ["India", "Australia", "Pak", "Sri Lanka",
           "England", "Bangladesh"]

# perform period_range() function
match_date = pd.period_range('8/1/2020', '8/6/2020', freq='D')

# generates dataframes
df = pd.DataFrame(country, index=match_date, columns=['Country'])

df
```
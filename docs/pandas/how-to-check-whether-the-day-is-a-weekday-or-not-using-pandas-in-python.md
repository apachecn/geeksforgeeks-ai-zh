# 如何使用 Python 中的 Pandas 检查当天是否为工作日？

> 原文:[https://www . geeksforgeeks . org/如何检查一天是工作日还是不使用 python 熊猫/](https://www.geeksforgeeks.org/how-to-check-whether-the-day-is-a-weekday-or-not-using-pandas-in-python/)

Python 是一种非常流行的语言，因为它几乎适用于任何类型的数据科学任务。Pandas 是流行的基于 python 的数据分析工具包之一，并且还提供了 **pandas.bdate_range()** 函数来返回固定频率的 DatetimeIndex。此函数返回固定频率的日期时间索引，以工作日(周一至 Fri)为默认频率。

> **语法:**pandas . bdate _ range(start =None，end=None，periods=None，freq='B '，tz=None，normalize=True，name=None，weekmask=None，节假日= None，closed=None，**kwargs)
> 
> **参数:**
> 
> **开始**:字符串或类似日期时间，默认无。
> 
> **end** :字符串或类似日期时间，默认无。
> 
> **周期**:整数，默认无。
> 
> **freq** :字符串或 DateOffset，默认为‘B’(商报)。
> 
> **tz** :字符串或无。
> 
> **正常化** : bool，默认 False
> 
> **名称**:字符串，默认无
> 
> **周掩码**:字符串或无，默认无
> 
> **节假日**:列表式或无，默认无

**进场:**

*   导入熊猫模块
*   创建一个返回布尔值的参数函数
*   检查给定日期是否在函数内部使用 pd.bdate_range()返回布尔值
*   检查布尔值是否为假，则日期属于工作日。如果布尔值为真，则不是工作日

下面是实现。

## 蟒蛇 3

```py
# importing Pandas module
import pandas as pd

# Creating a Function
def check_weekday(date):

    # computing the parameter date
    # with len function
    res=len(pd.bdate_range(date,date))

    if res == 0 :
        print("This is weekend")
    else:
        print("This is your working day") 

# user input
date = "2020-08-17"
check_weekday(date)

date = "2020-08-16"
check_weekday(date)
```

**输出:**

```py
This is your working day
This is weekend
```
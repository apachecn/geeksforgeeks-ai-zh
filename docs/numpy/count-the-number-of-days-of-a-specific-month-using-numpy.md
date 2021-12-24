# 使用 NumPy

统计特定月份的天数

> 原文:[https://www . geeksforgeeks . org/count-特定月份的天数-使用-numpy/](https://www.geeksforgeeks.org/count-the-number-of-days-of-a-specific-month-using-numpy/)

为了统计特定月份的天数，我们将使用 *numpy* 模块的 [numpy.datetime64()](https://www.geeksforgeeks.org/python-numpy-datetime64-method/) 方法。

**示例:**

```py
Input: month = 2; year = 2016
Output: 29 days

Input: month = 12; year = 2020
Output: 31 days
```

假设我们要计算天数的月份是 **P** ，下个月是 **N.** 我们将从该月的第一个日期 **N** 中减去该月的第一个日期 **P** 。在 *numpy.datetime64()* 方法中实现。

**语法:**

除 12 月以外的所有月份:

```py
numpy.datetime64('yyyy-N-01') - numpy.datetime64(yyyy-P-01')
```

12 月份:

```py
numpy.datetime64('yyyy-P-31') - numpy.datetime64(yyyy-P-01') + 1
```

#### 以下是描述如何使用 *numpy* 模块计算特定月份天数的各种示例:

**示例#1:**

在本例中，我们将找到 2016 年 2 月的天数。

## 蟒蛇 3

```py
# import module
import numpy

# explicit function to calculate
# number of days
def calcDays(month, year):
    date = 0

    # December case
    if month == 12:
        end = str(year)+'-'+str(month)+'-31'
        begin = str(year)+'-'+str(month)+'-01'
        date = 1
    else:

        # single digit months
        if month < 10:
            endM = '-0'+str(month+1)
            beginM = '-0'+str(month)

        # double digit months
        else:
            endM = '-'+str(month+1)
            beginM = '-'+str(month)

        end = str(year)+endM+'-01'
        begin = str(year)+beginM+'-01'

    # return number of days
    return (numpy.datetime64(end) - numpy.datetime64(begin)+date)

# Driver Code

# get month
month = 2

# get year
year = 2016

# call the function
print(calcDays(month, year))
```

**输出:**

```py
29 days
```

**例 2:**

在这里，我们将找到 2001 年 4 月的天数。

## 蟒蛇 3

```py
# import module
import numpy

# explicit function to calculate
# number of days
def calcDays(month, year):
    date = 0

    # December case
    if month == 12:
        end = str(year)+'-'+str(month)+'-31'
        begin = str(year)+'-'+str(month)+'-01'
        date = 1
    else:

        # single digit months
        if month < 10:
            endM = '-0'+str(month+1)
            beginM = '-0'+str(month)

        # double digit months
        else:
            endM = '-'+str(month+1)
            beginM = '-'+str(month)

        end = str(year)+endM+'-01'
        begin = str(year)+beginM+'-01'

    # return number of days
    return (numpy.datetime64(end) - numpy.datetime64(begin)+date)

# Driver Code

# get month
month = 4

# get year
year = 2001

# call the function
print(calcDays(month, year))
```

**输出:**

```py
30 days
```

**示例#3:**

在下面的程序中，我们将找到 2021 年 12 月的天数。

## 蟒蛇 3

```py
# import module
import numpy

# explicit function to calculate
# number of days
def calcDays(month, year):
    date = 0

    # December case
    if month == 12:
        end = str(year)+'-'+str(month)+'-31'
        begin = str(year)+'-'+str(month)+'-01'
        date = 1
    else:

        # single digit months
        if month < 10:
            endM = '-0'+str(month+1)
            beginM = '-0'+str(month)

        # double digit months
        else:
            endM = '-'+str(month+1)
            beginM = '-'+str(month)

        end = str(year)+endM+'-01'
        begin = str(year)+beginM+'-01'

    # return number of days
    return (numpy.datetime64(end) - numpy.datetime64(begin)+date)

# Driver Code

# get month
month = 12

# get year
year = 2021

# call the function
print(calcDays(month, year))
```

**输出:**

```py
31 days
```
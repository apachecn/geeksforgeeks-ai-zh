# 使用 NumPy

找到给定月份的工作日数

> 原文:[https://www . geeksforgeeks . org/find-给定月份的工作日数-使用-numpy/](https://www.geeksforgeeks.org/find-the-number-of-weekdays-of-a-given-month-using-numpy/)

在 NumPy 中，我们可以在 busday_count()的帮助下找到给定月份的工作日数。在此过程中，给定月份是第一个参数，下个月是第二个参数。它将返回给定月份的工作日总数。

> **语法:**
> 
> numpy.busday_count ( *开始日期* 、 *结束日期* 、 *周掩码* )
> 
> **参数:**
> 
> 开始日期:用于计数的第一个日期的数组。
> 
> 结束日期:计数的结束日期数组，从计数本身中排除。
> 
> 周掩码:选择日期

工作日仅从周一到周五。

**示例#1:**

## 蟒蛇 3

```py
import numpy as np

# Number of weekdays in july 2020
print("Number of weekdays in july 2020:",
      np.busday_count('2020-07', '2020-08'))
```

**输出:**

```py
Number of weekdays in july 2020: 23

```

**例 2:** 我们可以用这个星期掩码来统计 Sat 的个数。

## 蟒蛇 3

```py
import numpy as np

# Number of weekdays in August 2020
print("Number of saturday in november 2020:",
      np.busday_count('2020-11', '2020-12',
                      weekmask='Sat'))
```

**输出:**

```py
Number of saturday in november 2020: 4

```

**例 3:** 统计周日的次数。

## 蟒蛇 3

```py
import numpy as np

# Number of weekdays in August 2020
print("Number of Sunday in november 2020:",
      np.busday_count('2020-11', '2020-12',
                      weekmask='Sun'))
```

**输出:**

```py
Number of Sunday in november 2020: 5

```
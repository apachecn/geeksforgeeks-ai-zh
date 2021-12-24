# 使用 NumPy

显示特定月份的所有日期

> 原文:[https://www . geeksforgeeks . org/display-特定月份的所有日期-使用-numpy/](https://www.geeksforgeeks.org/display-all-the-dates-for-a-particular-month-using-numpy/)

在 NumPy 中，为了显示特定月份的所有日期，我们可以在[NumPy . array()](https://www.geeksforgeeks.org/numpy-arange-python/)的帮助下完成，传递第一个参数特定月份和第二个参数下个月，第三个参数是数据类型 datetime64[D]。它将返回特定月份的所有日期。

> **语法:**numpy . array(*start*、】 *stop* 、【 *step* 、】*dtype = None*)
> 
> **参数:**
> 
> **开始:** 开始间隔
> 
> **停止:** 间隔结束
> 
> **步长:**值之间的间距
> 
> **数据类型:** 输出数组的类型。如果没有给出 [数据类型](https://numpy.org/doc/stable/reference/generated/numpy.dtype.html#numpy.dtype) ，从其他输入参数中推断数据类型。
> 
> **返回:**
> 
> **排列:**ndaarray

**例 1#:**

## 蟒蛇 3

```py
import numpy as np

# dates of july  2020
print(np.arrange('2012-07', '2020-08',
                dtype='datetime64[D]'))
```
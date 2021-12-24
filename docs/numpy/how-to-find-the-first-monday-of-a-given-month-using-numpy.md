# 如何使用 NumPy 查找给定月份的第一个星期一？

> 原文:[https://www . geeksforgeeks . org/如何使用 numpy 找到给定月份的第一个星期一/](https://www.geeksforgeeks.org/how-to-find-the-first-monday-of-a-given-month-using-numpy/)

为了找到给定月份的第一个星期一，我们将使用 [*numpy*](https://www.geeksforgeeks.org/numpy-in-python-set-1-introduction/) 模块，即 *numpy* 模块中的 *numpy.busday_offset()* 方法。

> **语法:** np.busday_offset('date '，0，roll='forward '，weekmask='Mon ')
> 
> **参数:**
> 
> **日期:**要处理的日期数组。
> 
> **偏移量:**偏移量数组，与日期一起广播。
> 
> **滚动:**取以下值:
> 
> *   **提出**表示针对无效日提出异常。
> *   **nat** 表示在无效的一天返回一个 nat(不是一次)。
> *   **向前****跟随**意味着在时间上更晚的时候取第一个有效日。
> *   **向后****在**之前表示提前第一个有效日。
> *   **modifiedfollowing** 的意思是在时间上较晚取第一个有效日，除非它跨越一个月边界，在这种情况下在时间上较早取第一个有效日。
> *   **modified previous**表示在时间上提前第一个有效日，除非它跨越月边界，在这种情况下，在时间上推迟第一个有效日。
> 
> **weekmask:** 数组，指示周一到周日中的哪一天是有效日期。
> 
> **返回(datetime64 的 out array):**一个数组，其形状由广播日期和偏移量组成，包含应用了偏移量的日期。

#### 下面是一些使用 *numpy.busday_offset()* 方法获取一个月的第一个星期一的程序:

**示例#1:**

在本例中，我们将找到 2017 年 5 月的第一个星期一。

## 蟒蛇 3

```
# import module
import numpy

# input year and month
yearMonth = '2017-05'

# getting date of first monday
date = numpy.busday_offset(yearMonth, 0, 
                           roll='forward', 
                           weekmask='Mon')

# display date
print(date)
```
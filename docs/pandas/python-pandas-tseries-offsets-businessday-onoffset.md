# Python | Pandas tseries . offset . business day . onoffset

> 原文:[https://www . geesforgeks . org/python-pandas-ts eries-offset-business day-onoffset/](https://www.geeksforgeeks.org/python-pandas-tseries-offsets-businessday-onoffset/)

日期偏移量是熊猫中用于日期范围的一种标准的日期增量。就我们传递的关键字 args 而言，它的工作原理与 relativedelta 完全一样。日期偏移量的工作原理如下，每个偏移量指定一组符合日期偏移量的日期。例如， *Bday* 将该集合定义为工作日(M-F)的日期集合。

可以创建日期偏移量来将日期向前移动给定的有效日期数。例如，可以将 *Bday(2)* 添加到日期中，使其提前两个工作日。如果日期没有在有效日期开始，则首先将其移动到有效日期，然后创建偏移。

熊猫 `**tseries.offsets.BusinessDay.onOffset()**`函数返回一个布尔值。如果给定的工作日偏移在偏移上，则返回`True`，否则返回`False`

> **语法:**pandas . tseries . offset . business day . onoffset()
> 
> **参数:**无
> 
> **返回:**布尔值

**示例#1:** 使用`pandas.tseries.offsets.BusinessDay.onOffset()`功能检查给定的工作日偏移对象是否偏移。

```py
# importing pandas as pd
import pandas as pd

# Creating Timestamp
ts = pd.Timestamp('2019-10-10 07:15:11')

# Create an offset of 5 Business days
bd = pd.tseries.offsets.BusinessDay(n = 5)

# Print the Timestamp
print(ts)

# Print the DateOffset
print(bd)
```

**输出:**

![](img/31fa9e80203f8bb21b39d4385472bd28.png)

![](img/1d1737a5d0b06b452ab379d87f50258d.png)

现在，我们将向给定的时间戳对象添加工作日偏移量，以增加日期时间值。我们还将检查给定的工作日偏移对象是否处于偏移状态。

```py
# Adding the Business day offset to the given timestamp
new_timestamp = ts + bd

# Print the updated timestamp
print(new_timestamp)

# check if the offset is 
# on offset or not
result = bd.onOffset()

# print the result
print(result)
```

**输出:**

![](img/d10efe783a87515533a70042bbdd85cc.png)

![](img/2134f1326ee7fbc4388c96657e61fcb9.png)

正如我们在输出中看到的，我们已经成功地创建了一个 5 个工作日的偏移量，并将其添加到给定的时间戳中。给定函数已返回`False`，表示给定偏移对象不在偏移上。

**示例 2 :** 使用`pandas.tseries.offsets.BusinessDay.onOffset()`功能检查给定的工作日偏移对象是否偏移。

```py
# importing pandas as pd
import pandas as pd

# Creating Timestamp
ts = pd.Timestamp('2019-10-10 07:15:11')

# Create an offset of 10 Business days and 10 hours
bd = pd.tseries.offsets.BusinessDay(offset = datetime.timedelta(days = 10, hours = 10))

# Print the Timestamp
print(ts)

# Print the DateOffset
print(bd)
```

**输出:**

![](img/31fa9e80203f8bb21b39d4385472bd28.png)

![](img/3ddc56673632c0084372bea2f71ab964.png)

现在，我们将向给定的时间戳对象添加工作日偏移量，以增加日期时间值。我们还将检查给定的工作日偏移对象是否处于偏移状态。

```py
# Adding the Business day offset to the given timestamp
new_timestamp = ts + bd

# Print the updated timestamp
print(new_timestamp)

# check if the offset is 
# on offset or not
result = bd.onOffset()

# print the result
print(result)
```

**输出:**

![](img/28a71a7149304daec7031eb0c4d37537.png)

![](img/2134f1326ee7fbc4388c96657e61fcb9.png)

正如我们在输出中看到的，我们已经成功地创建了 10 个工作日& 10 个小时的偏移量，并将其添加到给定的时间戳中。给定函数已返回`False`，表示给定偏移对象不在偏移上。
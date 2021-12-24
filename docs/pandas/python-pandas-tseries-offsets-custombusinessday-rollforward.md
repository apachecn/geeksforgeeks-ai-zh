# Python | Pandas tseries . offset . custom business day . roll forward

> 原文:[https://www . geesforgeks . org/python-pandas-ts eries-offset-custom business day-roll forward/](https://www.geeksforgeeks.org/python-pandas-tseries-offsets-custombusinessday-rollforward/)

日期偏移量是熊猫中用于日期范围的一种标准的日期增量。就我们传递的关键字 args 而言，它的工作原理与 relativedelta 完全一样。日期偏移的工作方式如下，每个偏移指定一组符合日期偏移的日期。例如， *Bday* 将该集合定义为工作日(M-F)的日期集合。

可以创建日期偏移量来将日期向前移动给定的有效日期数。例如，可以将 *Bday(2)* 添加到日期中，使其提前两个工作日。如果日期没有在有效日期开始，则首先将其移动到有效日期，然后创建偏移。

熊猫 `**tseries.offsets.CustomBusinessDay.rollforward()**`功能仅在不偏移时提供向前到下一个偏移的日期滚动。

> **语法:**pandas . tseries . offset . custom business day . roll forward(dt)
> 
> **参数:**
> **dt :** 日期
> 
> **返回:**如果没有偏移，则前滚

**示例#1:** 如果给定的时间戳不在偏移量上，使用`pandas.tseries.offsets.CustomBusinessDay.rollforward()`函数向前滚动。

```
# importing pandas as pd
import pandas as pd

# Creating Timestamp
ts = pd.Timestamp('2019-4-23 11:15:00')

# Create an offset
cbd = pd.tseries.offsets.CustomBusinessDay(weekmask = 'Mon Tue Wed')

# Print the Timestamp
print(ts)

# Print the Offset
print(cbd)
```

**输出:**

![](img/e0dfb84ec590773846b3cb253771ae92.png)

![](img/e4d25fefe80b4e002628a48cfe74d635.png)

现在，我们将向给定的时间戳对象添加偏移量，以增加日期时间值。如果给定的时间戳不在偏移量上，我们也将前滚。

```
# Adding the offset to the given timestamp
new_timestamp = ts + cbd

# Print the updated timestamp
print(new_timestamp)

# roll forward if the given timestamp
# is not on offset
result = cbd.rollforward(pd.Timestamp('2019-4-21 11:15:00'))

# print the result
print(result)
```

**输出:**

![](img/678b87bf35f5af7eef3a4778610a7ac4.png)

![](img/76d1aabc7babd4c30595c29a1d8f806d.png)

正如我们在输出中看到的，我们已经成功地创建了一个偏移量，并将其添加到给定的时间戳中。我们还向前滚动了给定的时间戳，因为它不在偏移量上。

**示例#2:** 如果给定的时间戳不在偏移量上，使用`pandas.tseries.offsets.CustomBusinessDay.rollforward()`函数向前滚动。

```
# importing pandas as pd
import pandas as pd

# Creating Timestamp
ts = pd.Timestamp('2019-4-23 11:15:00')

# Create an offset
cbd = pd.tseries.offsets.CustomBusinessDay(n = 3, weekmask = 'Mon Tue Wed Thu')

# Print the Timestamp
print(ts)

# Print the Offset
print(cbd)
```

**输出:**

![](img/e0dfb84ec590773846b3cb253771ae92.png)

![](img/16f0fd2f37fad9429a47343fb3b578d0.png)

现在，我们将向给定的时间戳对象添加偏移量，以增加日期时间值。如果给定的时间戳不在偏移量上，我们也将前滚。

```
# Adding the offset to the given timestamp
new_timestamp = ts + cbd

# Print the updated timestamp
print(new_timestamp)

# roll forward if the given timestamp
# is not on offset
result = cbd.rollforward(pd.Timestamp('2019-4-21 11:15:00'))

# print the result
print(result)
```

**输出:**

![](img/1ad8a9e1b9ad28012d5010124bc691b4.png)

![](img/76d1aabc7babd4c30595c29a1d8f806d.png)

正如我们在输出中看到的，我们已经成功地创建了一个偏移量，并将其添加到给定的时间戳中。我们还向前滚动了给定的时间戳，因为它不在偏移量上。
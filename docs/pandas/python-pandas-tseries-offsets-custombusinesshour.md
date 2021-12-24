# Python | Pandas tseries . offset . custombusiness hour

> 原文:[https://www . geesforgeks . org/python-pandas-ts eries-offset-custombusiness hour/](https://www.geeksforgeeks.org/python-pandas-tseries-offsets-custombusinesshour/)

日期偏移量是熊猫中用于日期范围的一种标准的日期增量。就我们传递的关键字 args 而言，它的工作原理与 relativedelta 完全一样。日期偏移的工作方式如下，每个偏移指定一组符合日期偏移的日期。例如， *Bday* 将该集合定义为工作日(M-F)的日期集合。

可以创建日期偏移量来将日期向前移动给定的有效日期数。例如，可以将 *Bday(2)* 添加到日期中，使其提前两个工作日。如果日期没有在有效日期开始，则首先将其移动到有效日期，然后创建偏移。

熊猫 `**tseries.offsets.CustomBusinessHour()**`功能用于创建自己的定制营业时间。表示可能 n 个自定义工作日的 DateOffset 子类。

> **语法:**pandas . tseries . offset . custombusiness hour()
> 
> **参数:**
> **n:**int
> **Normalize:**在生成日期范围
> **之前将开始/结束日期规范化为午夜周掩码:**有效工作日的周掩码，传递给 numpy.busdaycalendar
> **节假日:**无
> **日历:**无
> **开始:**营业时间开始
> **结束:**
> 
> **返回:**偏移量

**示例#1:** 使用`pandas.tseries.offsets.CustomBusinessHour()`功能创建您自己的自定义营业时间偏移。

```py
# importing pandas as pd
import pandas as pd

# Creating Timestamp
ts = pd.Timestamp('2019-4-23 11:15:00')

# Create an offset
cbh = pd.tseries.offsets.CustomBusinessHour(n = 2, weekmask = 'Mon Tue Wed Thu',
                                           start ='12:00')

# Print the Timestamp
print(ts)

# Print the Offset
print(cbh)
```

**输出:**

![](img/e0dfb84ec590773846b3cb253771ae92.png)

![](img/4a18519f44fcbd1022ab3d34ee6834a3.png)

现在，我们将向给定的时间戳对象添加偏移量，以增加日期时间值。

```py
# Adding the offset to the given timestamp
new_timestamp = ts + cbh

# Print the updated timestamp
print(new_timestamp)
```

**输出:**

![](img/a30fa80851ee6ae90dbb5c876ec32328.png)

正如我们在输出中看到的，我们已经成功地创建了一个偏移量，并将其添加到给定的时间戳中。

**示例 2:** 使用`pandas.tseries.offsets.CustomBusinessHour()`功能创建您自己的自定义营业时间偏移。

```py
# importing pandas as pd
import pandas as pd

# Creating Timestamp
ts = pd.Timestamp('2019-4-23 11:15:00')

# Create an offset
cbh = pd.tseries.offsets.CustomBusinessHour(start ='07:00', end ='14:00')

# Print the Timestamp
print(ts)

# Print the Offset
print(cbh)
```

**输出:**

![](img/e0dfb84ec590773846b3cb253771ae92.png)

![](img/32e224c371cc0f205d6d43ed7ea7995b.png)

现在，我们将向给定的时间戳对象添加偏移量，以增加日期时间值。

```py
# Adding the offset to the given timestamp
new_timestamp = ts + cbh

# Print the updated timestamp
print(new_timestamp)
```

**输出:**

![](img/df360b6011955f9fe78ba406d14502d2.png)

正如我们在输出中看到的，我们已经成功地创建了一个偏移量，并将其添加到给定的时间戳中。
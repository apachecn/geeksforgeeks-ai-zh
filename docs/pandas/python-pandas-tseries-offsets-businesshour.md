# 蟒蛇|熊猫 tseries . offers . business hour

> 原文:[https://www . geesforgeks . org/python-pandas-ts eries-offset-business hour/](https://www.geeksforgeeks.org/python-pandas-tseries-offsets-businesshour/)

日期偏移量是熊猫中用于日期范围的一种标准的日期增量。就我们传递的关键字 args 而言，它的工作原理与 relativedelta 完全一样。日期偏移的工作方式如下，每个偏移指定一组符合日期偏移的日期。例如， *Bday* 将该集合定义为工作日(M-F)的日期集合。

可以创建日期偏移量来将日期向前移动给定的有效日期数。例如，可以将 *Bday(2)* 添加到日期中，使其提前两个工作日。如果日期没有在有效日期开始，则首先将其移动到有效日期，然后创建偏移。

熊猫 `**tseries.offsets.BusinessHour()**`功能用于创建营业时间的偏移。

> **语法:**pandas . tseries . offset . business hour(n = 1，normalize=False，start='09:00 '，end='17:00 '，offset=datetime.timedelta(0))
> 
> **参数:**
> **n :** 小时数
> **归一化:**是否将日期偏移量相加的结果四舍五入到前一个午夜。
> **开始:**开始时间
> **结束:**结束时间
> **偏移:**从给定日期偏移
> 
> **返回:**偏移量

**示例#1:** 使用`pandas.tseries.offsets.BusinessHour()`功能创建 5 个工作时间的偏移量。

```py
# importing pandas as pd
import pandas as pd

# Creating Timestamp
ts = pd.Timestamp('2019-10-10 07:15:11')

# Create an offset of 5 Business hours
bh = pd.tseries.offsets.BusinessHour(n = 5)

# Print the Timestamp
print(ts)

# Print the Offset
print(bh)
```

**输出:**

![](img/31fa9e80203f8bb21b39d4385472bd28.png)

![](img/d0f27a69e6773625bcb85c0632d91b5b.png)

现在，我们将业务时间偏移量添加到给定的时间戳对象中，以增加日期时间值。

```py
# Adding the Business hour offset to the given timestamp
new_timestamp = ts + bh

# Print the updated timestamp
print(new_timestamp)
```

**输出:**

![](img/a222282f6886a4d7624b109ec5dfe365.png)

正如我们在输出中看到的，我们已经成功地创建了一个 5 个工作小时的偏移量，并将其添加到给定的时间戳中。

**示例 2:** 使用`pandas.tseries.offsets.BusinessHour()`功能创建 10 天 5 个工作时间的偏移量。

```py
# importing pandas as pd
import pandas as pd

# Creating Timestamp
ts = pd.Timestamp('2019-10-10 07:15:11')

# Create an offset
bh = pd.tseries.offsets.BusinessHour(offset = datetime.timedelta(days = 10, hours = 10))

# Print the Timestamp
print(ts)

# Print the Offset
print(bh)
```

**输出:**

![](img/31fa9e80203f8bb21b39d4385472bd28.png)

![](img/4014d121bd834fb327962fad19af6d44.png)

现在，我们将业务时间偏移量添加到给定的时间戳对象中，以增加日期时间值。

```py
# Adding the Business hour offset to the given timestamp
new_timestamp = ts + bh

# Print the updated timestamp
print(new_timestamp)
```

**输出:**

![](img/20acc2ef2646ece661e321ef22835e61.png)

正如我们在输出中看到的，我们已经成功地创建了一个偏移量，并将其添加到给定的时间戳中。
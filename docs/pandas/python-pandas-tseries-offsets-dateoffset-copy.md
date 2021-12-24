# Python |熊猫 tseries . offsets . date offset . copy

> 原文:[https://www . geeksforgeeks . org/python-pandas-ts eries-offset-date offset-copy/](https://www.geeksforgeeks.org/python-pandas-tseries-offsets-dateoffset-copy/)

日期偏移量是熊猫中用于日期范围的一种标准的日期增量。就我们传递的关键字 args 而言，它的工作原理与 relativedelta 完全一样。日期偏移的工作方式如下，每个偏移指定一组符合日期偏移的日期。例如， *Bday* 将该集合定义为工作日(M-F)的日期集合。

可以创建日期偏移量来将日期向前移动给定的有效日期数。例如，可以将 *Bday(2)* 添加到日期中，使其提前两个工作日。如果日期没有在有效日期开始，则首先将其移动到有效日期，然后创建偏移。

熊猫 `**tseries.offsets.DateOffset.copy()**`函数返回给定日期偏移对象的副本。

> **语法:**pandas . tseries . offset . datepoffset . copy()
> 
> **参数:**无
> 
> **返回:**给定对象的副本

**示例#1:** 使用`pandas.tseries.offsets.DateOffset.copy()`函数返回给定日期偏移对象的副本。

```py
# importing pandas as pd
import pandas as pd

# importing the to_offset function
from pandas.tseries.frequencies import to_offset

# Creating Timestamp
ts = pd.Timestamp('2019-10-10 07:15:11')

# Create the DateOffset of 2 day
do = to_offset(freq = '2D')

# Print the Timestamp
print(ts)

# Print the DateOffset
print(do)
```

**输出:**

![](img/31fa9e80203f8bb21b39d4385472bd28.png)

![](img/641db2d690673a06debc51be5e69a4aa.png)

现在，我们将向给定的时间戳对象添加 dateoffset，以增加 datetime 值。我们还将返回给定日期偏移对象的副本。

```py
# Adding the dateoffset to the given timestamp
new_timestamp = ts + do

# Print the updated timestamp
print(new_timestamp)

# Now we will create a copy of the given
# DateOffset object.
do_copy = do.copy()

# Check if the two objects are same or not
print(do_copy is do)
```

**输出:**

![](img/245c467c7299064278ddbe002c2f1fc9.png)

![](img/17f0fb7d12501a02dc9d0903de5438be.png)

正如我们在输出中看到的，该函数已经成功创建了给定 Dateoffset 对象的副本。`False`表示两个物体不相同。

**示例#2:** 使用`pandas.tseries.offsets.DateOffset.copy()`函数返回给定日期偏移对象的副本。

```py
# importing pandas as pd
import pandas as pd

# importing the to_offset function
from pandas.tseries.frequencies import to_offset

# Creating Timestamp
ts = pd.Timestamp('2019-10-10 07:15:11')

# Create the DateOffset
do = to_offset(freq = '10D2H')

# Print the Timestamp
print(ts)

# Print the DateOffset
print(do)
```

**输出:**

![](img/31fa9e80203f8bb21b39d4385472bd28.png)

![](img/4219c63f4fbfe0cc5086f9ee784635d7.png)

现在，我们将向给定的时间戳对象添加 dateoffset，以增加 datetime 值。我们还将返回给定日期偏移对象的副本。

```py
# Adding the dateoffset to the given timestamp
new_timestamp = ts + do

# Print the updated timestamp
print(new_timestamp)

# Now we will create a copy of the given
# DateOffset object.
do_copy = do.copy()

# Check if the two objects are same or not
print(do_copy is do)
```

**输出:**

![](img/c88d2610c30e211cd40048e79386c646.png)

![](img/17f0fb7d12501a02dc9d0903de5438be.png)

正如我们在输出中看到的，该函数已经成功创建了给定 Dateoffset 对象的副本。`False`表示两个物体不相同。
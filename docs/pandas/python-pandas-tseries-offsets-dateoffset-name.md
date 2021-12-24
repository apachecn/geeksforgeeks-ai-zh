# Python |熊猫 tseries . offsets . date offset . name

> 原文:[https://www . geeksforgeeks . org/python-pandas-tseries-offset-datept-name/](https://www.geeksforgeeks.org/python-pandas-tseries-offsets-dateoffset-name/)

日期偏移量是熊猫中用于日期范围的一种标准的日期增量。就我们传递的关键字 args 而言，它的工作原理与 relativedelta 完全一样。日期偏移的工作方式如下，每个偏移指定一组符合日期偏移的日期。例如， *Bday* 将该集合定义为工作日(M-F)的日期集合。

可以创建日期偏移量来将日期向前移动给定的有效日期数。例如，可以将 *Bday(2)* 添加到日期中，使其提前两个工作日。如果日期没有在有效日期开始，则首先将其移动到有效日期，然后创建偏移。

Pandas `**tseries.offsets.DateOffset.name**`属性允许您在函数中使用偏移量以简化操作，而不是导入和初始化类。它还返回应用于偏移对象的频率名称。

> **语法:**pandas . tseries . offset . datepoffset . name
> 
> **参数:**无
> 
> **返回:**名称

**示例#1:** 使用`pandas.tseries.offsets.DateOffset.name`属性返回应用于给定日期偏移对象的频率名称。

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

现在，我们将向给定的时间戳对象添加 dateoffset，以从给定的日期向前滚动日期。还返回应用于给定日期偏移对象的频率名称。

```py
# Adding the dateoffset to the given timestamp
new_timestamp = ts + do

# Print the updated timestamp
print(new_timestamp)

# Now we will print the name of the frequency
# applied on the given DateOffset object
print(do.name)
```

**输出:**

![](img/245c467c7299064278ddbe002c2f1fc9.png)

![](img/8b35f08bd8e1aa3a7b13008f567a53ac.png)

正如我们在输出中看到的，属性已经成功地返回了应用于给定 Dateoffset 对象的频率名称。

**示例#2:** 使用`pandas.tseries.offsets.DateOffset.name`属性返回应用于给定 DateOffset 对象的关键字参数。

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

现在，我们将向给定的时间戳对象添加 dateoffset，以从给定的日期向前滚动日期。还返回应用于给定日期偏移对象的频率名称。

```py
# Adding the dateoffset to the given timestamp
new_timestamp = ts + do

# Print the updated timestamp
print(new_timestamp)

# Now we will print the name of the frequency
# applied on the given DateOffset object
print(do.name)
```

**输出:**

![](img/c88d2610c30e211cd40048e79386c646.png)

![](img/fd3b157b85f35d5be6ae1f95ff66af32.png)

正如我们在输出中看到的，属性已经成功地返回了应用于给定 Dateoffset 对象的频率名称。
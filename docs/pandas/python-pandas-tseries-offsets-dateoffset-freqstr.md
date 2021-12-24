# Python |熊猫 tseries . offsets . dateoffset . freqstr

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python 熊猫-tseries 偏移-dateoffset-freqstr/

日期偏移量是熊猫中用于日期范围的一种标准的日期增量。就我们传递的关键字 args 而言，它的工作原理与 relativedelta 完全一样。日期偏移的工作方式如下，每个偏移指定一组符合日期偏移的日期。例如， *Bday* 将该集合定义为工作日(M-F)的日期集合。

可以创建日期偏移量来将日期向前移动给定的有效日期数。例如，可以将 *Bday(2)* 添加到日期中，使其提前两个工作日。如果日期没有在有效日期开始，则首先将其移动到有效日期，然后创建偏移。

Pandas `**tseries.offsets.DateOffset.freqstr**`属性将频率对象作为给定日期偏移对象的字符串返回。

> **语法:**pantas . tseries . offset . dateoffset . freqstr
> 
> **参数:**无
> 
> **返回:**作为字符串应用的频率对象

**示例#1:** 使用`pandas.tseries.offsets.DateOffset.freqstr`属性以字符串形式返回应用于给定日期偏移对象的频率对象。

```
# importing pandas as pd
import pandas as pd

# Creating Timestamp
ts = pd.Timestamp('2019-10-10 07:15:11')

# Create the DateOffset
do = pd.tseries.offsets.DateOffset(n = 2)

# Print the Timestamp
print(ts)

# Print the DateOffset
print(do)
```

**输出:**

![](img/31fa9e80203f8bb21b39d4385472bd28.png)

![](img/e179ed982fa52f5bca021fecb6227e71.png)

现在，我们将把 dateoffset 添加到给定的 timestamp 对象中，以从给定的日期创建一个 2 天的偏移量。还返回应用于给定日期偏移对象的频率。

```
# Adding the dateoffset to the given timestamp
new_timestamp = ts + do

# Print the updated timestamp
print(new_timestamp)

# Now we will find the freqstr
print(do.freqstr)
```

**输出:**

![](img/245c467c7299064278ddbe002c2f1fc9.png)

![](img/ce1dbd20a99139addc55224f21281483.png)

正如我们在输出中看到的，属性已经成功地返回了作为字符串应用于给定 DateOffset 对象的频率。

**示例#2:** 使用`pandas.tseries.offsets.DateOffset.freqstr`属性以字符串形式返回应用于给定日期偏移对象的频率对象。

```
# importing pandas as pd
import pandas as pd

# Creating Timestamp
ts = pd.Timestamp('2019-10-10 07:15:11')

# Create the DateOffset
do = pd.tseries.offsets.DateOffset(days = 10, hours = 2)

# Print the Timestamp
print(ts)

# Print the DateOffset
print(do)
```

**输出:**

![](img/31fa9e80203f8bb21b39d4385472bd28.png)

![](img/23fb61877bba29436fbba85e80eb7d09.png)

现在，我们将把 dateoffset 添加到给定的 timestamp 对象中，以从给定的日期创建一个 2 天的偏移量。还返回应用于给定日期偏移对象的频率。

```
# Adding the dateoffset to the given timestamp
new_timestamp = ts + do

# Print the updated timestamp
print(new_timestamp)

# Now we will find the freqstr
print(do.freqstr)
```

**输出:**

![](img/245c467c7299064278ddbe002c2f1fc9.png)

![](img/31c61580c1ffe3083b3c4d857d8289d0.png)

正如我们在输出中看到的，属性已经成功地返回了作为字符串应用于给定 DateOffset 对象的频率。
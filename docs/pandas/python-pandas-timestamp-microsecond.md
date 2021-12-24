# Python | Pandas Timestamp .微秒

> 原文:[https://www . geesforgeks . org/python-pandas-timestamp-微秒/](https://www.geeksforgeeks.org/python-pandas-timestamp-microsecond/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**Timestamp.microsecond**`属性返回给定时间戳对象中微秒的值。

> **语法:**时间戳.微秒
> 
> **参数:**无
> 
> **返回:**微秒

**示例#1:** 使用`Timestamp.microsecond`属性在给定的 Timestamp 对象中查找微秒值。

```
# importing pandas as pd
import pandas as pd

# Create the Timestamp object
ts = pd.Timestamp(2016, 1, 1, 12, 25, 16, 28)

# Print the Timestamp object
print(ts)
```

**输出:**

![](img/560adf225074c9294b4b17c8396b5d9c.png)

现在我们将使用`Timestamp.microsecond`属性打印 ts 对象中微秒的值。

```
# find the value of microsecond
ts.microsecond
```

**输出:**

![](img/dcf580ace0fa99ec08ae1e5e9b6f15d6.png)

我们可以在输出中看到，`Timestamp.microsecond`属性返回了 28，表示 ts 对象中的微秒值设置为 28。

**示例#2:** 使用`Timestamp.microsecond`属性在给定的时间戳对象中查找微秒值。

```
# importing pandas as pd
import pandas as pd

# Create the Timestamp object
ts = pd.Timestamp(year = 2009, month = 5, day = 31, hour = 4,
                      microsecond = 15, tz = 'Europe/Berlin')

# Print the Timestamp object
print(ts)
```

**输出:**

![](img/393c9a89327505271a3d60f53168731d.png)

现在我们将使用`Timestamp.microsecond`属性打印 ts 对象中微秒的值。

```
# find the value of microsecond
ts.microsecond
```

**输出:**

![](img/783757deffd15f4be583c0d1d4e97869.png)

我们可以在输出中看到，`Timestamp.microsecond`属性返回了 15，表示 ts 对象中的微秒值设置为 15。
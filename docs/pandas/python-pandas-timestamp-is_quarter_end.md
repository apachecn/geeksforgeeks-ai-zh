# Python | Pandas timestamp . is _ quarter _ end

> 原文:[https://www . geesforgeks . org/python-pandas-timestamp-is _ quarter _ end/](https://www.geeksforgeeks.org/python-pandas-timestamp-is_quarter_end/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**Timestamp.is_quarter_end**`属性返回一个布尔值。如果给定时间戳对象中的日期是季度末，则返回`True`，否则返回`False`。

> **语法:** Timestamp.is_quarter_end
> 
> **参数:**无
> 
> **返回:**布尔值

**示例#1:** 使用`Timestamp.is_quarter_end`属性检查给定时间戳对象中的日期是否是季度末。

```py
# importing pandas as pd
import pandas as pd

# Create the Timestamp object
ts = pd.Timestamp(2016, 3, 31, 12)

# Print the Timestamp object
print(ts)
```

**输出:**

![](img/4610b12077b93e83ea8ce7fcc76f808d.png)

现在我们将使用`Timestamp.is_quarter_end`属性来检查 ts 对象中的日期是否是季度末。

```py
# check if the date is quarter end or not
ts.is_quarter_end
```

**输出:**

![](img/dfd6c229eb8dbab8aa1db53c056cbb54.png)

正如我们在输出中看到的那样，`Timestamp.is_quarter_end`属性返回了`True`，表示给定 Timestamp 对象中的日期是季度末

**示例#2:** 使用`Timestamp.is_quarter_end`属性检查给定时间戳对象中的日期是否是季度末。

```py
# importing pandas as pd
import pandas as pd

# Create the Timestamp object
ts = pd.Timestamp(year = 2009, month = 5, day = 31,
                    hour = 4, tz = 'Europe/Berlin')

# Print the Timestamp object
print(ts)
```

**输出:**

![](img/a8ba805f9246e9bfc00fc2cb9a018978.png)

现在我们将使用`Timestamp.is_quarter_end`属性来检查 ts 对象中的日期是否是季度末。

```py
# check if the date is quarter end or not
ts.is_quarter_end
```

**输出:**

![](img/11c1cccddcda2d6fd3725fbcbf8d3a5d.png)

正如我们在输出中看到的那样，`Timestamp.is_quarter_end`属性返回了`False`，表明给定 Timestamp 对象中的日期不是季度末。
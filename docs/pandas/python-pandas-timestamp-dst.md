# Python |熊猫时间戳. dst

> 原文:[https://www.geeksforgeeks.org/python-pandas-timestamp-dst/](https://www.geeksforgeeks.org/python-pandas-timestamp-dst/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**Timestamp.dst()**`函数返回一个包含 self.tzinfo.dst(self)值的 timedelta 对象。它返回给定时间戳对象时区的夏令时。

> **语法:** Timestamp.dst()
> 
> **参数:**无
> 
> 退货: dst

**示例#1:** 使用`Timestamp.dst()`函数查找给定时间戳对象的夏令时。

```py
# importing pandas as pd
import pandas as pd

# Create the Timestamp object
ts = pd.Timestamp('2015-03-31 15:47:25.901597', tz = 'US/Eastern')

# Print the Timestamp object
print(ts)
```

**输出:**

![](img/895e8eff8c030848ebc81bc1696c4058.png)

现在我们将使用`Timestamp.dst()`函数来查找给定对象的 dst。

```py
# return the dst
ts.dst()
```

**输出:**

![](img/9ad180b34ea5d655ba560703fb6ef278.png)

正如我们在输出中看到的那样，`Timestamp.dst()`函数返回了一个 timedelta 对象，该对象包含给定 Timestamp 对象的夏令时。

**示例 2:** 使用`Timestamp.dst()`函数查找给定时间戳对象的夏令时。

```py
# importing pandas as pd
import pandas as pd

# Create the Timestamp object
ts = pd.Timestamp(year = 2009,  month = 5, day = 31, 
        hour = 4, second = 49, tz = 'Europe/Berlin')

# Print the Timestamp object
print(ts)
```

**输出:**

![](img/e2c4d93f6eeb606ab122d97734870a13.png)

现在我们将使用`Timestamp.dst()`函数来查找给定对象的 dst。

```py
# return the dst
ts.dst()
```

**输出:**

![](img/9ad180b34ea5d655ba560703fb6ef278.png)

正如我们在输出中看到的那样，`Timestamp.dst()`函数返回了一个 timedelta 对象，该对象包含给定 Timestamp 对象的夏令时。
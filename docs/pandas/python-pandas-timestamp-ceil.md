# 蟒蛇|熊猫时间戳. ceil

> 原文:[https://www.geeksforgeeks.org/python-pandas-timestamp-ceil/](https://www.geeksforgeeks.org/python-pandas-timestamp-ceil/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**Timestamp.ceil()**`函数返回一个新的时间戳，以此为分辨率。该函数将所需的时间序列频率作为输入。

> **语法:** Timestamp.ceil()
> 
> **参数:**
> **freq :** 表示天花板分辨率的 freq 字符串
> 
> **返回:**时间戳

**示例#1:** 使用`Timestamp.ceil()`函数将给定的时间戳对象上限为每日时间序列频率。

```
# importing pandas as pd
import pandas as pd

# Create the Timestamp object
ts = pd.Timestamp(year = 2011,  month = 11, day = 21,
           hour = 10, second = 49, tz = 'US/Central')

# Print the Timestamp object
print(ts)
```

**输出:**

![](img/ee694c9af88333eeafa810576fa77c25.png)

现在我们将使用`Timestamp.ceil()`功能将 ts 对象提升到每日频率。

```
# ceil the given object to daily frequency
ts.ceil(freq ='D')
```

**输出:**

![](img/414b6c7eae97e4cca0e8631ab59e88ed.png)

正如我们在输出中看到的，`Timestamp.ceil()`函数已经将给定 Timestamp 对象的时间序列频率转换为输入频率。

**示例#2:** 使用`Timestamp.ceil()`函数将给定的时间戳对象上限为分钟时间序列频率。

```
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

现在我们将使用`Timestamp.ceil()`功能将 ts 对象提升到微小频率。

```
# ceil the given object to minutely frequency
ts.ceil(freq ='T')
```

**输出:**

![](img/cdbdfd2fcfe5c7cfbbcd2c13bb688a36.png)

正如我们在输出中看到的，`Timestamp.ceil()`函数已经将给定 Timestamp 对象的时间序列频率转换为输入频率。
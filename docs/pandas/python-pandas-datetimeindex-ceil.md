# python | pandas dateindex . ceil()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python 熊猫-date index-ceil/

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**DatetimeIndex.ceil()**`功能将数据提升到指定频率。该函数以目标频率为输入。它返回一个新的日期时间索引对象。

> **语法:** DatetimeIndex.ceil(freq)
> 
> **参数:**
> **频率:**将频率等级提升到上限指数。必须是固定频率，如“S”(秒)而不是“ME”(月末)
> 
> **返回:**一个日期时间索引或时间增量索引的相同类型的索引，或者一个序列具有相同索引的序列

**示例#1:** 使用`DatetimeIndex.ceil()`函数将 DatetimeIndex 对象的数据提升到指定的频率。

```py
# importing pandas as pd
import pandas as pd

# Create the DatetimeIndex
# Here 'S' represents secondly frequency 
didx = pd.DatetimeIndex(start ='2000-01-15 08:00', freq ='S', periods = 4)

# Print the DatetimeIndex
print(didx)
```

**输出:**
![](img/fec3f998f15f4a0d44089bada6ddd968.png)

现在，我们希望将 DatetimeIndex 对象的第二个频率限制为分钟频率

```py
# convert to the passed frequency
# 'T' represents minute based frequency
didx.ceil('T')
```

**输出:**
![](img/8656b0e002e6674b27a67523ee4a72bc.png)

正如我们在输出中看到的，该函数返回了 DatetimeIndex 对象的上限值。

**示例 2:** 使用`DatetimeIndex.ceil()`函数将 DatetimeIndex 对象的数据提升到指定的频率。

```py
# importing pandas as pd
import pandas as pd

# Create the DatetimeIndex
# Here 'T' represents minutely frequency 
didx = pd.DatetimeIndex(start ='2018-11-15 09:45', freq ='T', periods = 5)

# Print the DatetimeIndex
print(didx)
```

**输出:**
![](img/12c25cd333feff1d372b96c81fd5ce2c.png)

现在我们希望将 DatetimeIndex 对象基于分钟的频率上限为基于小时的频率

```py
# ceil the given frequency
didx.ceil('H')
```

**输出:**
![](img/cc093782f5a285bc8469fad61edf2970.png)
正如我们在输出中看到的，函数已经将 DatetimeIndex 对象的值提升到了所需的频率。
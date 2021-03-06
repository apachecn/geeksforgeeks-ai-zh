# python \ panda datetimeindex . day ofweek】的缩写形式

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python 熊猫约会索引-dayofweek/

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**DatetimeIndex.dayofweek**`属性为 DatetimeIndex 对象的每个条目输出一周中某一天的序号值。周一到周日的值范围从 0 到 6。

> **语法：** 日期时间索引.星期一
> 
> **返回:**索引对象

**示例#1:** 使用`DatetimeIndex.dayofweek`属性为 DatetimeIndex 对象中的每个条目查找一周中某一天的序号值。

```py
# importing pandas as pd
import pandas as pd

# Create the DatetimeIndex
# Here 'D' represents Daily frequency
didx = pd.DatetimeIndex(start ='2000-01-10 06:30', freq ='D', 
                            periods = 3, tz ='Asia/Calcutta')

# Print the DatetimeIndex
print(didx)
```

**输出:**
![](img/6a02ef51f8ccf8e7ac6e5d07670a48b9.png)

现在，我们想要为 DatetimeIndex 对象中的每个条目找到一周中的每一天的序号值。

```py
# find the ordinal value of the day 
# of the week for each entries present in the object
didx.dayofweek
```

**输出:**
![](img/64a26de6880ef359f7e3c2506aa33363.png)
正如我们在输出中看到的，该函数返回了一个 Index 对象，该对象包含 DatetimeIndex 对象的每个条目的星期几的顺序值。

**示例#2:** 使用`DatetimeIndex.dayofweek`属性为 DatetimeIndex 对象中的每个条目查找一周中某一天的序号值。

```py
# importing pandas as pd
import pandas as pd

# Create the DatetimeIndex
# Here 'M' represents monthly frequency
didx = pd.DatetimeIndex(start ='2014-08-01 10:05:45', freq ='M',
                               periods = 5, tz ='Asia/Calcutta')

# Print the DatetimeIndex
print(didx)
```

**输出:**
![](img/7209b56d19803e90e9ddf2e50319c2e7.png)
现在我们想要为 DatetimeIndex 对象中的每个条目找到一周中的每一天的序数值。

```py
# find the ordinal value of the day of the week
# for each entries present in the object
didx.dayofweek
```

**输出:**
![](img/197029054b17b8e59213b3924fe60baf.png)
正如我们在输出中看到的，该函数返回了一个 Index 对象，该对象包含 DatetimeIndex 对象的每个条目的星期几的序数值。
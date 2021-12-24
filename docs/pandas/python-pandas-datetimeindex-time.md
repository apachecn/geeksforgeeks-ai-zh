# python | pandas dateindex . time

时间

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-panda-dateindex-time/

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**DatetimeIndex.time**`属性输出一个索引对象，该对象包含出现在 DatetimeIndex 对象的每个条目中的时间值。

> **语法：** 日期时间索引.时间
> 
> **返回:**python datetime . time 的 numpy 数组

**示例#1:** 使用`DatetimeIndex.time`属性查找 DatetimeIndex 对象的时间部分。

```py
# importing pandas as pd
import pandas as pd

# Create the DatetimeIndex
# Here 'H' represents hourly frequency
didx = pd.DatetimeIndex(start ='2000-01-10 06:30', freq ='H', 
                            periods = 3, tz ='Asia/Calcutta')

# Print the DatetimeIndex
print(didx)
```

**输出:**
![](img/e89d6f258cd169c8d50e5972f2476902.png)

现在我们想找到 DatetimeIndex 对象的所有时间部分。

```py
# find all the time values present in the object
didx.time
```

**输出:**
![](img/36b1f3a551c181e6dac3170c432aac19.png)
正如我们在输出中看到的，该函数返回了一个 Index 对象，该对象包含 DatetimeIndex 对象的每个条目中存在的时间值。

**示例#2:** 使用`DatetimeIndex.time`属性查找 DatetimeIndex 对象的时间部分。

```py
# importing pandas as pd
import pandas as pd

# Create the DatetimeIndex
# Here 's' represents secondly frequency
didx = pd.DatetimeIndex(start ='2014-08-01 10:05:45', freq ='S',
                              periods = 5, tz ='Asia/Calcutta')

# Print the DatetimeIndex
print(didx)
```

**输出:**
![](img/e493fe5ab0ca08bb059ea51d5dccf486.png)

现在我们想找到 DatetimeIndex 对象的所有时间部分。

```py
# find all the time values present in the object
didx.time
```

**输出:**
![](img/0286a70fbddf3041e6b060bf511938b5.png)
正如我们在输出中看到的，该函数返回了一个 Index 对象，该对象包含 DatetimeIndex 对象的每个条目中存在的时间值。
# Python |熊猫约会指数。freq

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python 熊猫约会索引-freq/

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**DatetimeIndex.freq**`属性返回频率对象，如果它是在 DatetimeIndex 对象中设置的。如果未设置频率，则返回无。

> **语法：** 日期时间索引.freq
> 
> **返回:**频率对象

**示例#1:** 使用`DatetimeIndex.freq`属性查找给定日期时间索引对象的频率。

```
# importing pandas as pd
import pandas as pd

# Create the DatetimeIndex
# Here 'BQ' represents Business quarter frequency
didx = pd.DatetimeIndex(start ='2014-08-01 10:05:45', freq ='BQ', 
                               periods = 5, tz ='Asia/Calcutta')

# Print the DatetimeIndex
print(didx)
```

**输出:**
![](img/83edcb931a1a0699837fe183d00d6eb9.png)

现在我们想找到给定的 DatetimeIndex 对象的频率值。

```
# find the value of frequency
didx.freq
```

**输出:**
![](img/b87dce60b01c08e1670d084b4fddaf46.png)
正如我们在输出中看到的，函数已经为给定的 DatetimeIndex 对象返回了一个 frequency 对象。

**示例#2:** 使用`DatetimeIndex.freq`属性为给定的 DatetimeIndex 对象查找频率。

```
# importing pandas as pd
import pandas as pd

# Create the DatetimeIndex
# Here 'CBMS' represents custom business month start frequency
didx = pd.DatetimeIndex(start ='2000-01-10 06:30', freq ='CBMS',
                               periods = 5, tz ='Asia/Calcutta')

# Print the DatetimeIndex
print(didx)
```

**输出:**
![](img/f4a42c851d0a8132b1e387964be2b2e0.png)
现在我们要找到给定 DatetimeIndex 对象的频率值。

```
# find the value of frequency
didx.freq
```

**输出:**
![](img/db50907ee733f9ba0f738b9e615a00aa.png)
正如我们在输出中看到的，函数已经为给定的 DatetimeIndex 对象返回了一个 frequency 对象。didx DatetimeIndex 对象具有自定义的业务月开始频率。
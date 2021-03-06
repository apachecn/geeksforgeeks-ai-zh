# Python |熊猫时间差指数. ceil

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python 熊猫-timedeltaindex-ceil/

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**TimedeltaIndex.ceil()**`函数将时间增量索引对象的索引增加到指定的频率。该函数将频率作为一个参数，我们希望对其取最大值。

> **语法:** TimedeltaIndex.ceil(freq)
> 
> **参数:**
> **freq :** freq 字符串/对象
> 
> **返回:**同类型索引

**示例#1:** 使用`TimedeltaIndex.ceil()`函数将给定时间增量索引对象的值上限为指定频率。

```py
# importing pandas as pd
import pandas as pd

# Create the first TimedeltaIndex object
tidx = pd.TimedeltaIndex(start ='1 days 02:00:12.001124', periods = 5,
                                            freq ='N', name ='Koala')

# Print the TimedeltaIndex object
print(tidx)
```

**输出:**
![](img/fa501ab75d1da1cbef90ba6ba12024c4.png)

现在，我们将使用`TimedeltaIndex.ceil()`功能将数值上限为每分钟一次。

```py
# ceil the values to minutely frequency.
tidx.ceil('T')
```

**输出:**
![](img/f7e0641a17e844eaa32246f6874638f5.png)
正如我们在输出中看到的那样，`TimedeltaIndex.ceil()`函数返回了一个新的索引对象，该对象包含以所需频率为中心的值。

**示例 2:** 使用`TimedeltaIndex.ceil()`函数将给定时间增量索引对象的值上限为指定频率。

```py
# importing pandas as pd
import pandas as pd

# Create the TimedeltaIndex object
tidx = pd.TimedeltaIndex(data =['06:05:01.000030', '+23:59:59.999999',
                                      '22 day 2 min 3us 10ns', None])

# Print the TimedeltaIndex object
print(tidx)
```

**输出:**
![](img/dd2772b998fbfdf2bcba17cad4207713.png)

现在我们将使用`TimedeltaIndex.ceil()`功能将数值上限为每日频率。

```py
# ceil the values to daily frequency.
tidx.ceil('D')
```

**输出:**
![](img/fe6b09fb1396f2d8315699a9bb6d4118.png)
正如我们在输出中看到的那样，`TimedeltaIndex.ceil()`函数返回了一个新的索引对象，该对象包含的值已经达到了所需的频率。
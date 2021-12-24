# python | pandas time delta index . view()

> 哎哎哎::1230【https://www . geeksforgeeks . org/python 熊猫-时间增量索引视图/

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**TimedeltaIndex.view()**`功能用于给定时间增量索引对象的可视化。这就像打印对象。

> **语法**时标索引. view(cls=None)
> 
> **参数:**无
> 
> **返回:**视图

**示例#1:** 使用`TimedeltaIndex.view()`函数可视化给定的时间增量索引对象。

```
# importing pandas as pd
import pandas as pd

# Create the TimedeltaIndex object
tidx = pd.TimedeltaIndex(data =['06:05:01.000030', '+23:59:59.999999',
                        '22 day 2 min 3us 10ns', '06:05:01.000030',
                        '+12:19:59.999999'])

# Print the TimedeltaIndex object
print(tidx)
```

**输出:**
![](img/bfa2cde8f5c996874f45ca911d82f1e9.png)

现在我们将使用`TimedeltaIndex.view()`功能来查看 tidx 对象

```
# print the TimedeltaIndex object 
tidx.view()
```

**输出:**
![](img/bfa2cde8f5c996874f45ca911d82f1e9.png)

从输出中我们可以看到，`TimedeltaIndex.view()`函数基本上已经在屏幕上打印了给定的 TimedeltaIndex 对象。

**示例 2:** 使用`TimedeltaIndex.view()`函数可视化给定的时间增量索引对象。

```
# importing pandas as pd
import pandas as pd

# Create the TimedeltaIndex object
tidx = pd.TimedeltaIndex(data =['3 days 06:05:01.000030','1 days 06:05:01.000030',
                        '3 days 06:05:01.000030', '1 days 06:05:01.000030',
                        '21 days 06:15:01.000030'])

# Print the TimedeltaIndex object
print(tidx)
```

**输出:**
![](img/4c04ad3c32eac7d5d81d5580d3ad6e4e.png)

现在我们将使用`TimedeltaIndex.view()`功能来查看 tidx 对象

```
# print the TimedeltaIndex object 
tidx.view()
```

**输出:**
![](img/4c04ad3c32eac7d5d81d5580d3ad6e4e.png)
在输出中我们可以看到，`TimedeltaIndex.view()`功能已经基本上把给定的 TimedeltaIndex 对象打印到了屏幕上。
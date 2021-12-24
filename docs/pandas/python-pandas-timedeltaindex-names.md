# python \ panda 时标索引.名称

> 原文:[https://www . geesforgeks . org/python-pandas-time delta index-names/](https://www.geeksforgeeks.org/python-pandas-timedeltaindex-names/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**TimedeltaIndex.names**`属性返回一个包含时间增量索引对象名称的冻结列表(如果已设置)。如果没有为所考虑的对象设置名称，则返回无。

> **语法:t1】timedeletendex . names**
> 
> **返回:** frozenlist

**示例#1:** 使用`TimedeltaIndex.names`属性找出时间增量索引对象的名称。

```py
# importing pandas as pd
import pandas as pd

# Create the TimedeltaIndex object
tidx = pd.TimedeltaIndex(data =['1 days 02:00:00', '1 days 06:05:01.000030', 
                                      '1 days 02:00:00'], name ='MyObjejct')

# Print the TimedeltaIndex
print(tidx)
```

**输出:**
![](img/791b6df69a1c4f1b363b8cb6534c1dbc.png)

现在我们将找出 tidx 对象的名称

```py
# print the names of the TimedeltaIndex object.
tidx.names
```

**输出:**
![](img/cceb983b0818b732f7a0b3ab0c53d16e.png)
在输出中我们可以看到，`TimedeltaIndex.names`属性已经返回了对象的名称。

**例 2:** 使用`TimedeltaIndex.names`属性找出 TimedeltaIndex 对象的名称。

```py
# importing pandas as pd
import pandas as pd

# Create the TimedeltaIndex object
tidx = pd.TimedeltaIndex(start ='1 days 02:00:00', periods = 5, 
                                       freq ='T', name ='Koala')

# Print the TimedeltaIndex
print(tidx)
```

**输出:**
![](img/26b4ef0e8e62e43780c7847e5661e83b.png)

现在我们将找出 tidx 对象的名称

```py
# print the name of the TimedeltaIndex object.
tidx.names
```

**输出:**
![](img/999152810f19e7d4c6673dcaa1512b62.png)
在输出中我们可以看到，`TimedeltaIndex.names`属性已经返回了对象的名称。
# Python | Pandas time deltaindex . is _ unique

> 原文:[https://www . geesforgeks . org/python-pandas-time deltaindex-is _ unique/](https://www.geeksforgeeks.org/python-pandas-timedeltaindex-is_unique/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**TimedeltaIndex.is_unique**`属性检查时间增量索引中的所有条目是否唯一。如果条目不唯一，则返回`False`值，否则返回`True`值。

> **语法:**时间增量索引. is_unique
> 
> **返回:**布尔值

**示例#1:** 使用`TimedeltaIndex.is_unique`属性检查时间增量索引对象中的条目是否唯一。

```py
# importing pandas as pd
import pandas as pd

# Create the TimedeltaIndex object
tidx = pd.TimedeltaIndex(start ='1 days 02:00:00', periods = 5, freq ='T')

# Print the TimedeltaIndex
print(tidx)
```

**输出:**
![](img/2edf6147730bd28456b4797fe3d2f5d9.png)

现在我们将检查时间增量索引对象是否包含唯一的条目。

```py
# check if tidx is containing unique values or not.
tidx.is_unique
```

**输出:**
![](img/5507be7e27f61a843c1cf5dc48d34011.png)

我们可以在输出中看到，`TimedeltaIndex.is_unique`属性已经返回了`True`，表示 tidx 对象中的值是唯一的。

**示例 2:** 使用`TimedeltaIndex.is_unique`属性检查时间增量索引对象中的条目是否唯一。

```py
# importing pandas as pd
import pandas as pd

# Create the TimedeltaIndex object
tidx = pd.TimedeltaIndex(data =['1 days 02:00:00', '1 days 06:05:01.000030',
                                                        '1 days 02:00:00'])

# Print the TimedeltaIndex
print(tidx)
```

**输出:**
![](img/0f69d05dcd1f9bcad4ce3d4fcfd72093.png)

现在我们将检查时间增量索引对象是否包含唯一的条目。

```py
# check if tidx is containing unique values or not.
tidx.is_unique
```

**输出:**
![](img/3e5222c679e32dcaf3e86c0e0d0ef4ca.png)
正如我们在输出中看到的，`TimedeltaIndex.is_unique`属性返回了`False`，表示 tidx 对象中的值不是唯一的。
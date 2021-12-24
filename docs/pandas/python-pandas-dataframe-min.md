# python | pandas data frame . min()

> 原文:[https://www.geeksforgeeks.org/python-pandas-dataframe-min/](https://www.geeksforgeeks.org/python-pandas-dataframe-min/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**dataframe.min()**`函数返回给定对象中的最小值。如果输入是一个序列，该方法将返回一个标量，该标量将是该序列中值的最小值。如果输入是数据帧，则该方法将返回数据帧中指定轴上最小值的系列。默认情况下，轴是索引轴。

> **语法:** DataFrame.min(轴=无，skipna =无，级别=无，numeric _ only =无，**kwargs)
> **参数:**
> **轴:**沿给定轴将对象与阈值对齐。
> **skipna :** 计算结果时排除 NA/null 值
> **级别:**如果轴是 MultiIndex(分层)，沿特定级别计数，折叠成 Series
> **numeric _ only:**仅包括 float、int、boolean 列。如果没有，将尝试使用所有内容，然后只使用数字数据。
> 系列未执行。
> 
> **返回:**分钟:序列或数据帧(如果指定了级别)

**示例#1:** 使用`min()`函数查找索引轴上的最小值。

```py
# importing pandas as pd
import pandas as pd

# Creating the dataframe 
df = pd.DataFrame({"A":[12, 4, 5, 44, 1],
                   "B":[5, 2, 54, 3, 2], 
                   "C":[20, 16, 7, 3, 8], 
                   "D":[14, 3, 17, 2, 6]})

# Print the dataframe
df
```

![](img/06fb933825fd3c59f9328866de87d49e.png)

让我们使用`dataframe.min()`函数找到索引轴上的最小值

```py
# find min Even if we do not specify axis = 0, the method 
# will return the min over the index axis by default
df.min(axis = 0)
```

**输出:**
![](img/00200986714a5eb5598babad1a4fe826.png)

**示例 2:** 对具有`Na`值的数据框使用`min()`功能。还要找到柱轴上的最小值。

```py
# importing pandas as pd
import pandas as pd

# Creating the dataframe 
df = pd.DataFrame({"A":[12, 4, 5, None, 1],
                   "B":[7, 2, 54, 3, None],
                   "C":[20, 16, 11, 3, 8], 
                   "D":[14, 3, None, 2, 6]})

# Print the dataframe
df
```

![](img/e093b7a9e106096a3cc650fe549a1cbe.png)

让我们实现 min 函数。

```py
# skip the Na values while finding the minimum
df.min(axis = 1, skipna = True)
```

**输出:**
![](img/5686891cf4e1ce1bde757ef091e2a953.png)
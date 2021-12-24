# Python | Pandas period index . weekday

> 原文:[https://www . geesforgeks . org/python-pandas-period index-weekday/](https://www.geeksforgeeks.org/python-pandas-periodindex-weekday/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

Pandas `**PeriodIndex.weekday**`属性返回一个包含一周中某一天的 Index 对象，对于给定 PeriodIndex 对象中的每个 period 元素，周一=0 到周日=6。

> **语法:** PeriodIndex.weekday
> 
> **参数:**无
> 
> **返回:**索引对象

**示例#1:** 使用`PeriodIndex.weekday`属性找出给定 PeriodIndex 对象中每个周期元素的星期几。

```
# importing pandas as pd
import pandas as pd

# Create the PeriodIndex object
pidx = pd.PeriodIndex(start ='2004-11-11 02:45:21 ', 
               end ='2004-11-21 8:45:29', freq ='D')

# Print the PeriodIndex object
print(pidx)
```

**输出:**
![](img/e450cb83bc7578514d3e77f8b331051e.png)

现在我们将使用`PeriodIndex.weekday`属性为 pidx 对象中的每个周期元素查找星期几。

```
# return the day of the week
pidx.weekday
```

**输出:**
![](img/d36bc55c44cf64ad366104c1d0786162.png)

正如我们在输出中看到的那样，`PeriodIndex.weekday`属性返回了一个 Index 对象，该对象包含给定 PeriodIndex 对象中包含的每个 period 元素的星期几。

**示例 2:** 使用`PeriodIndex.weekday`属性找出给定 PeriodIndex 对象中每个周期元素的星期几。

```
# importing pandas as pd
import pandas as pd

# Create the PeriodIndex object
pidx = pd.PeriodIndex(start ='2016-2-12 11:12:02',
            end ='2016-09-12 11:32:12', freq ='M')

# Print the PeriodIndex object
print(pidx)
```

**输出:**
![](img/a9b4b792185dbb89ed084839e4a77192.png)

现在我们将使用`PeriodIndex.weekday`属性为 pidx 对象中的每个周期元素查找星期几。

```
# return the day of the week
pidx.weekday
```

**输出:**

![](img/44ec638e3e7e69a8ae6ad3c613c01cf7.png)

正如我们在输出中看到的那样，`PeriodIndex.weekday`属性返回了一个 Index 对象，该对象包含给定 PeriodIndex 对象中包含的每个 period 元素的星期几。
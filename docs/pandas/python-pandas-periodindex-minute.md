# 蟒蛇|熊猫 PeriodIndex.minute

> 原文:[https://www . geesforgeks . org/python-pandas-period index-minute/](https://www.geeksforgeeks.org/python-pandas-periodindex-minute/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**PeriodIndex.minute**`属性返回一个索引对象，该对象包含给定周期索引对象中每个周期的分钟值。

> **语法:** PeriodIndex.minute
> 
> **参数:**无
> 
> **返回:**索引对象

**示例#1:** 使用`PeriodIndex.minute`属性找出给定周期索引对象中每个周期的分钟值。

```py
# importing pandas as pd
import pandas as pd

# Create the PeriodIndex object
pidx = pd.PeriodIndex(start ='2003-12-21 08:45 ',
               end ='2003-12-21 8:55', freq ='T')

# Print the PeriodIndex object
print(pidx)
```

**输出:**
![](img/ded2c635a0273396a0cf3664f44868fa.png)

现在我们将使用`PeriodIndex.minute`属性找出 pidx 中每个周期的分钟值。

```py
# find minute value
pidx.minute
```

**输出:**
![](img/504156683ffe9a78e33a64d68921e7cd.png)
正如我们在输出中看到的，`PeriodIndex.minute`属性有一个索引对象，包含给定 PeriodIndex 对象中每个周期的分钟值。

**示例 2:** 使用`PeriodIndex.minute`属性找出给定 PeriodIndex 对象中每个周期的分钟值。

```py
# importing pandas as pd
import pandas as pd

# Create the PeriodIndex object
pidx = pd.PeriodIndex(start ='2016-02-1 11:32', 
           end ='2016-02-01 11:55', freq ='T')

# Print the PeriodIndex object
print(pidx)
```

**输出:**
![](img/f7a8afc83ac4bea171bb491b8c7e4ef2.png)

现在我们将使用`PeriodIndex.minute`属性找出 pidx 中每个周期的分钟值。

```py
# find minute value
pidx.minute
```

**输出:**
![](img/9cb48b1c55d859bd14a685ab5431958d.png)

正如我们在输出中看到的那样，`PeriodIndex.minute`属性有一个索引对象，包含给定周期索引对象中每个周期的分钟值。
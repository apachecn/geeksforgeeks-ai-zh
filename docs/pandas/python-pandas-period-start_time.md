# 蟒蛇|熊猫 Period.start_time

> 原文:[https://www . geesforgeks . org/python-pandas-period-start _ time/](https://www.geeksforgeeks.org/python-pandas-period-start_time/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

Pandas `**Period.start_time**`属性返回一个包含给定周期对象开始时间的 Timestamp 对象。

> **语法:** Period.start_time
> 
> **参数:**无
> 
> **返回:**时间戳对象

**示例#1:** 使用`Period.start_time`属性查找给定周期对象的开始时间。

```
# importing pandas as pd
import pandas as pd

# Create the Period object
prd = pd.Period(freq ='S', year = 2000, month = 2, day = 22,
                         hour = 8, minute = 21, second = 24)

# Print the Period object
print(prd)
```

**输出:**

![](img/e74d8dfa72965f36f64b1d11a228d297.png)

现在我们将使用`Period.start_time`属性来查找 prd 对象的开始时间。

```
# return the start time
prd.start_time
```

**输出:**

![](img/9126aa281344d8f9fab82640660c2315.png)

正如我们在输出中看到的那样，`Period.start_time` 属性返回了一个 Timestamp 对象，该对象包含日期值以及给定周期对象的开始时间。

**示例#2:** 使用`Period.start_time`属性查找给定周期对象的开始时间。

```
# importing pandas as pd
import pandas as pd

# Create the Period object
prd = pd.Period(freq ='S', year = 2006, month = 10, 
               hour = 15, minute = 49, second = 17)

# Print the object
print(prd)
```

**输出:**

![](img/7752883a0d3bbe6723b83c640e79cd94.png)

现在我们将使用`Period.start_time`属性来查找 prd 对象的开始时间。

```
# return the start time
prd.start_time
```

**输出:**

![](img/63edf3aba32819ff4b1181fb80961ab9.png)

正如我们在输出中看到的那样，`Period.start_time` 属性返回了一个 Timestamp 对象，该对象包含日期值以及给定周期对象的开始时间。
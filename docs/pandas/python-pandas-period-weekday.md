# 蟒蛇|熊猫时期.工作日

> 原文:[https://www.geeksforgeeks.org/python-pandas-period-weekday/](https://www.geeksforgeeks.org/python-pandas-period-weekday/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

Pandas `**Period.weekday**`属性返回一个整数值，表示给定周期对象的工作日。

> **语法:** Period.weekday
> 
> **参数:**无
> 
> **返回:**工作日

**示例#1:** 使用`Period.weekday`属性找出给定期间对象中的工作日。

```py
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

现在我们将使用`Period.weekday`属性来查找 prd 对象中的工作日。

```py
# return the weekday
prd.weekday
```

**输出:**
![](img/c8714f31b75ba31f04b16087a515777f.png)

正如我们在输出中看到的那样，`Period.weekday` 属性返回了 1，表示给定的时间段是一周的第一天。

**例 2:** 使用`Period.weekday`属性找出给定期间对象中的工作日。

```py
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

现在我们将使用`Period.weekday`属性来查找 prd 对象中的工作日。

```py
# return the weekday
prd.weekday
```

**输出:**
![](img/80c6fc386e1c253a774a150d3140b9ab.png)

正如我们在输出中看到的，`Period.weekday` 属性返回了 6，表示给定的时间段是一周的第六天。
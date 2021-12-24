# 蟒蛇|熊猫时期. day fweek

> 原文:[https://www . geesforgeks . org/python-pandas-period-dayofweek/](https://www.geeksforgeeks.org/python-pandas-period-dayofweek/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**Period.dayofweek**` 属性返回给定周期对象的星期几。它返回一个整数值。

> **语法:**句点. dayofweek
> 
> **参数:**无
> 
> **返回:**一周中的某一天

**示例#1:** 使用`Period.dayofweek`属性在给定的 Period 对象中查找星期几。

```
# importing pandas as pd
import pandas as pd

# Create the Period object
prd = pd.Period(freq ='D', year = 2001, month = 1, day = 21)

# Print the Period object
print(prd)
```

**输出:**

![](img/93b87a4a79dcf7d76c41b363b7d298a0.png)

现在我们将使用`Period.dayofweek`属性来查找给定对象中的星期几。

```
# return the day value 
prd.dayofweek
```

**输出:**

![](img/e7b64256ec83c9a9163887b15f645528.png)

正如我们在输出中看到的，`Period.dayofweek`属性返回了 6，表示接下来的日期是一周的第 6 天。

**示例 2:** 使用`Period.dayofweek`属性在给定的 Period 对象中查找星期几。

```
# importing pandas as pd
import pandas as pd

# Create the Period object
prd = pd.Period(freq ='Q', year = 2006, quarter = 1)

# Print the object
print(prd)
```

**输出:**

![](img/872e5cfe93c11d77a915107c84a00d08.png)

现在我们将使用`Period.dayofweek`属性来查找给定对象中的星期几。

```
# return the day value 
prd.dayofweek
```

**输出:**
![](img/116555cc12077580c47437fd083bc42f.png)

正如我们在输出中看到的，`Period.dayofweek`属性返回了 4，表示接下来的日期是一周的第 4 天。
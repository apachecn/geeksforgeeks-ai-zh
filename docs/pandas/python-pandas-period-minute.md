# 蟒蛇|熊猫句号.分钟

> 原文:[https://www.geeksforgeeks.org/python-pandas-period-minute/](https://www.geeksforgeeks.org/python-pandas-period-minute/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**Period.minute**`属性返回一个整数值。返回值表示给定周期对象中的分钟数。

> **语法:**句点.分钟
> 
> **参数:**无
> 
> **返回:**分钟数

**示例#1:** 使用`Period.minute` 属性查找给定周期对象中的分钟值。

```
# importing pandas as pd
import pandas as pd

# Create the Period object
prd = pd.Period(freq ='S', year = 2000, month = 2, day = 21, hour = 8, minute = 21)

# Print the Period object
print(prd)
```

**输出:**

![](img/b2a6e0631e56e7bc2970f8e7faf169d1.png)

现在我们将使用`Period.minute`属性找出 prd 对象中存在的分钟值。

```
# find minute value
prd.minute
```

**输出:**

![](img/f876bedb4e3b4feda5753c25f43d68c3.png)

我们可以在输出中看到，`Period.minute` 属性返回了 21，表示给定周期对象中的分钟值是 21。

**示例#2:** 使用`Period.minute`属性查找给定周期对象中的分钟值。

```
# importing pandas as pd
import pandas as pd

# Create the Period object
prd = pd.Period(freq ='T', year = 2006, month = 10,
                            hour = 15, minute = 49)

# Print the Period object
print(prd)
```

**输出:**

![](img/68f561dba8f2f27eadb924c51d624034.png)

现在我们将使用`Period.minute`属性找出 prd 对象中存在的分钟值。

```
# find minute value
prd.minute
```

**输出:**

![](img/0ea25d9f8047fc79539c2a347e71cf8e.png)

我们可以在输出中看到，`Period.minute` 属性返回了 49，表示给定周期对象中的分钟值是 49。
# 蟒蛇|熊猫期.月 _ 日

> 原文:[https://www . geesforgeks . org/python-pandas-period-days _ in _ month/](https://www.geeksforgeeks.org/python-pandas-period-days_in_month/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**Period.days_in_month**`属性返回给定周期对象中一个月中的天数。

> **语法:** Period.days_in_month
> 
> **参数:**无
> 
> **返回:**天数

**示例#1:** 使用`Period.days_in_month`属性查找给定周期对象中当月的天数。

```
# importing pandas as pd
import pandas as pd

# Create the Period object
prd = pd.Period(freq ='D', year = 2001, month = 2, day = 21)

# Print the Period object
print(prd)
```

**输出:**

![](img/f0e1932f3c2706f75d56e7ef775bb754.png)

现在我们将使用`Period.days_in_month`属性来查找给定周期对象中表示的月份中存在的天数。

```
# return the number of days
prd.days_in_month
```

**输出:**

![](img/8a24891fb5f69a561726bfe03c67b8da.png)

我们可以在输出中看到，`Period.days_in_month`属性返回了 28，表示给定周期对象中表示的月份有 28 天。

**示例#2:** 使用`Period.days_in_month`属性查找给定周期对象中当月的天数。

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

现在我们将使用`Period.days_in_month`属性来查找给定周期对象中表示的月份中存在的天数。

```
# return the number of days
prd.days_in_month
```

**输出:**

![](img/75b749c4aad0b1275ebb0e7919cd501b.png)

我们可以在输出中看到，`Period.days_in_month`属性返回了 31，表示给定期间对象中表示的月份有 31 天。
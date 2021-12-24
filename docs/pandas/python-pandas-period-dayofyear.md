# 蟒蛇|熊猫大年初一

> 原文:[https://www . geesforgeks . org/python-pandas-period-dayofyear/](https://www.geeksforgeeks.org/python-pandas-period-dayofyear/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**Period.dayofyear**`属性返回给定周期对象的一年中的某一天。它返回一个整数值。

> **语法:**句点. day fyear
> 
> **参数:**无
> 
> **返回:**一年中的某一天

**示例#1:** 使用`Period.dayofyear`属性在给定的 Period 对象中查找一年中的某一天。

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

现在我们将使用`Period.dayofyear`属性在给定对象中查找一年中的某一天。

```
# return the day value 
prd.dayofyear
```

**输出:**

![](img/e924d2fc83e42d390d22ae1a3f96e807.png)

我们可以在输出中看到，`Period.dayofyear`属性返回了 21，表示后面的日期是一年中的第 21 天。

**示例#2:** 使用`Period.dayofyear`属性在给定的 Period 对象中查找一年中的某一天。

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

现在我们将使用`Period.dayofyear`属性在给定对象中查找一年中的某一天。

```
# return the day value 
prd.dayofyear
```

**输出:**

![](img/9bc67991b452abd70a7fe14e01e45f62.png)

我们可以在输出中看到，`Period.dayofyear`属性返回了 90，表示后面的日期是一年中的第 90 天。
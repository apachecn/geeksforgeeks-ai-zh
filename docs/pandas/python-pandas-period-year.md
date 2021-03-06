# 蟒蛇|熊猫时期.年份

> 原文:[https://www.geeksforgeeks.org/python-pandas-period-year/](https://www.geeksforgeeks.org/python-pandas-period-year/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**Period.year**`属性返回一个整数值，代表给定周期所在的年份。

> **语法:**期间.年
> 
> **参数:**无
> 
> **回归:**年

**示例#1:** 使用`Period.year` 属性查找给定周期对象的周期所在年份。

```py
# importing pandas as pd
import pandas as pd

# Create the Period object
prd = pd.Period(freq ='S', year = 2000, month = 2,
                  day = 21, hour = 8, minute = 21)

# Print the Period object
print(prd)
```

**输出:**

![](img/b2a6e0631e56e7bc2970f8e7faf169d1.png)

现在我们将使用`Period.year`属性来查找年份的值

```py
# return the year value
prd.year
```

**输出:**
![](img/324aa83f6cfeee02933e5d120317be8f.png)

正如我们在输出中看到的，`Period.year` 属性返回了 2000，表示给定的周期位于 2000 年。

**示例#2:** 使用`Period.year`属性查找给定周期对象的周期所在年份。

```py
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

现在我们将使用`Period.year`属性来查找年份的值

```py
# return the year
prd.year
```

**输出:**
![](img/dc69b8480bbe201a33f5316eb3b9948c.png)
正如我们在输出中所看到的，`Period.year` 属性返回了 2006 年，表示给定的时间段位于 2006 年。
# 蟒蛇|熊猫时差天

> 原文:[https://www.geeksforgeeks.org/python-pandas-timedelta-days/](https://www.geeksforgeeks.org/python-pandas-timedelta-days/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。Pandas 就是其中之一，它让数据的导入和分析变得更加容易。

时间增量是`datetime.timedelta`的一个子类，并且以类似的方式表现。它相当于熊猫的蟒蛇`datetime.timedelta`，在大多数情况下可以互换。`pandas.Timedelta`中的`Timedelta.days`属性用于返回天数。

> **语法:**时间增量天数
> 
> **参数:**无
> 
> **退货:**退货天数

**代码#1:**

```py
# importing pandas as pd 
import pandas as pd 

# Create the Timedelta object 
td = pd.Timedelta('3 days 06:05:01.000030') 

# Print the Timedelta object 
print(td) 

print(td.days)
```

**Output:**

```py
3 days 06:05:01.000030
3

```

**代码#2:**

```py
# importing pandas as pd 
import pandas as pd 

# Create the Timedelta object 
td = pd.Timedelta('1 days 7 hours') 

# Print the Timedelta object 
print(td) 

print(td.days)
```

**Output:**

```py
1 days 07:00:00
1

```

**代码#3:**

```py
# importing pandas as pd 
import pandas as pd 
import datetime

# Create the Timedelta object 
td = pd.Timedelta(datetime.timedelta(days = 3, hours = 7, seconds = 8)) 

# Print the Timedelta object 
print(td) 

print(td.days)
```

**Output:**

```py
3 days 07:00:08
3

```
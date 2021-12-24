# 蟒蛇|熊猫时间增量微秒

> 原文:[https://www . geesforgeks . org/python-pandas-time delta-微秒/](https://www.geeksforgeeks.org/python-pandas-timedelta-microseconds/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。Pandas 就是其中之一，它让数据的导入和分析变得更加容易。

时间增量是`datetime.timedelta`的一个子类，并且以类似的方式表现。它相当于熊猫的蟒蛇`datetime.timedelta`，在大多数情况下可以互换。`pandas.Timedelta`中的`Timedelta.microseconds`属性用于返回微秒数。

> **语法:**时间增量微秒
> 
> **参数:**无
> 
> **返回:**返回微秒数。

**代码#1:**

```py
# importing pandas as pd 
import pandas as pd 

# Create the Timedelta object 
td = pd.Timedelta('3 days 06:05:01.000030') 

# Print the Timedelta object 
print(td) 

print(td.microseconds)
```

**Output:**

```py
3 days 06:05:01.000030
30

```

**代码#2:**

```py
# importing pandas as pd 
import pandas as pd 

# Create the Timedelta object 
td = pd.Timedelta('1 days 7 hours 254.1245 seconds') 

# Print the Timedelta object 
print(td) 

print(td.microseconds)
```

**Output:**

```py
1 days 07:04:14.124500
124500

```

**代码#3:**

```py
# importing pandas as pd 
import pandas as pd 
import datetime

# Create the Timedelta object 
td = pd.Timedelta(datetime.timedelta(days = 3, hours = 7, seconds = 8, microseconds = 545)) 

# Print the Timedelta object 
print(td) 

print(td.microseconds)
```

**Output:**

```py
3 days 07:00:08.000545
545

```
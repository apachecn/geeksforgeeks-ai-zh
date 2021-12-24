# 蟒蛇|熊猫时间增量秒

> 原文:[https://www . geesforgeks . org/python-pandas-time delta-seconds/](https://www.geeksforgeeks.org/python-pandas-timedelta-seconds/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。Pandas 就是其中之一，它让数据的导入和分析变得更加容易。

时间增量是`datetime.timedelta`的一个子类，并且以类似的方式表现。它相当于熊猫的蟒蛇`datetime.timedelta`，在大多数情况下可以互换。 **`Timedelta.seconds`** 属性在`pandas.Timedelta`中用于返回秒数。

> **语法:**时间增量秒
> 
> **参数:**无
> 
> **返回:**返回秒数。

**代码#1:**

```
# importing pandas as pd 
import pandas as pd 

# Create the Timedelta object 
td = pd.Timedelta('3 days 06:05:01.000000111') 

# Print the Timedelta object 
print(td) 

print(td.seconds)
```

**Output:**

```
3 days 06:05:01.000000
21901

```

**代码#2:**

```
# importing pandas as pd 
import pandas as pd 

# Create the Timedelta object 
td = pd.Timedelta('7 days 15 min 3 s') 

# Print the Timedelta object 
print(td) 

print(td.seconds)
```

**Output:**

```
7 days 00:15:03
903

```

**代码#3:**

```
# importing pandas as pd 
import pandas as pd 
import datetime

# Create the Timedelta object 
td = pd.Timedelta(133, unit ='s')

# Print the Timedelta object 
print(td) 

print(td.seconds)
```

**Output:**

```
0 days 00:02:13
133

```
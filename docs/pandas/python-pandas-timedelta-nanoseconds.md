# 蟒蛇|熊猫时间增量纳秒

> 原文:[https://www . geesforgeks . org/python-pandas-time delta-纳秒/](https://www.geeksforgeeks.org/python-pandas-timedelta-nanoseconds/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。Pandas 就是其中之一，它让数据的导入和分析变得更加容易。

时间增量是`datetime.timedelta`的一个子类，并且以类似的方式表现。它相当于熊猫的蟒蛇`datetime.timedelta`，在大多数情况下可以互换。 **`Timedelta.nanoseconds`** 属性在`pandas.Timedelta`中用于返回纳秒数。

> **语法:**时间增量纳秒
> 
> **参数:**无
> 
> **返回:**返回纳秒数。

**代码#1:**

```py
# importing pandas as pd 
import pandas as pd 

# Create the Timedelta object 
td = pd.Timedelta('3 days 06:05:01.000000111') 

# Print the Timedelta object 
print(td) 

print(td.nanoseconds)
```

**Output:**

```py
3 days 06:05:01.000000
111

```

**代码#2:**

```py
# importing pandas as pd 
import pandas as pd 

# Create the Timedelta object 
td = pd.Timedelta('7 days 15 min 3 s 42 ns') 

# Print the Timedelta object 
print(td) 

print(td.nanoseconds)
```

**Output:**

```py
7 days 00:15:03.000000
42

```

**代码#3:**

```py
# importing pandas as pd 
import pandas as pd 
import datetime

# Create the Timedelta object 
td = pd.Timedelta(133, unit ='ns')

# Print the Timedelta object 
print(td) 

print(td.nanoseconds)
```

**Output:**

```py
0 days 00:00:00.000000
133

```
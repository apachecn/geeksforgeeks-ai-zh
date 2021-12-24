# 蟒蛇|熊猫时间增量组件

> 原文:[https://www . geesforgeks . org/python-pandas-time delta-components/](https://www.geeksforgeeks.org/python-pandas-timedelta-components/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。Pandas 就是其中之一，它让数据的导入和分析变得更加容易。

时间增量是`datetime.timedelta`的一个子类，并且以类似的方式表现。它相当于熊猫的蟒蛇`datetime.timedelta`，在大多数情况下可以互换。**`Timedelta.components``pandas.Timedelta`中的**属性用于返回一个名为类的组件。

> **语法:**时间增量组件
> 
> **参数:**无
> 
> **返回:**返回一个名为类双的组件

**代码#1:**

```
# importing pandas as pd 
import pandas as pd 

# Create the Timedelta object 
td = pd.Timedelta('3 days 06:05:01.000030') 

# Print the Timedelta object 
print(td) 

print(td.components)
```

**Output:**

> 3 天 06:05:01.000030
> 组件(天=3，小时=6，分=5，秒=1，毫秒=0，微秒=30，纳秒=0)

**代码#2:**

```
# importing pandas as pd 
import pandas as pd 

# Create the Timedelta object 
td = pd.Timedelta('1 days 7 hours') 

# Print the Timedelta object 
print(td) 

print(td.components)
```

**Output:**

> 1 天 07:00:00
> 组件(天=1，小时=7，分钟=0，秒=0，毫秒=0，微秒=0，纳秒=0)

**代码#3:**

```
# importing pandas as pd 
import pandas as pd 
import datetime

# Create the Timedelta object 
td = pd.Timedelta(datetime.timedelta(days = 3, hours = 7, seconds = 8)) 

# Print the Timedelta object 
print(td) 

print(td.components)
```

**Output:**

> 3 天 07:00:08
> 组件(天=3，小时=7，分钟=0，秒=8，毫秒=0，微秒=0，纳秒=0)
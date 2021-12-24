# Python |熊猫时间差。asm8

> 原文:[https://www.geeksforgeeks.org/python-pandas-timedelta-asm8/](https://www.geeksforgeeks.org/python-pandas-timedelta-asm8/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。Pandas 就是其中之一，它让数据的导入和分析变得更加容易。

时间增量是`datetime.timedelta`的一个子类，并且以类似的方式表现。它相当于熊猫的蟒蛇`datetime.timedelta`，在大多数情况下可以互换。 **`Timedelta.asm8`** 属性在`pandas.Timedelta`中用来返回一个 numpy *timedelta64* 数组视图。

> **语法:**时间差值. asm8
> 
> **参数:**无
> 
> **返回:** numpy timedelta64 数组视图

**代码#1:**

```py
# importing pandas as pd 
import pandas as pd 

# Create the Timedelta object 
td = pd.Timedelta('3 days 06:05:01.000030') 

# Print the Timedelta object 
print(td) 

print(td.asm8)
```

**Output:**

```py
3 days 06:05:01.000030
281101000030000 nanoseconds

```

**代码#2:**

```py
# importing pandas as pd 
import pandas as pd 

# Create the Timedelta object 
td = pd.Timedelta('1 days 7 hours') 

# Print the Timedelta object 
print(td) 

print(td.asm8)
```

**Output:**

```py
1 days 07:00:00
111600000000000 nanoseconds

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

print(td.asm8)
```

**Output:**

```py
3 days 07:00:08
284408000000000 nanoseconds

```
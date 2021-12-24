# 蟒蛇|熊猫 Timedelta.floor()

> 原文:[https://www . geesforgeks . org/python-pandas-time delta-floor/](https://www.geeksforgeeks.org/python-pandas-timedelta-floor/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。Pandas 就是其中之一，它让数据的导入和分析变得更加容易。

时间增量是`datetime.timedelta`的一个子类，并且以类似的方式表现。它相当于熊猫的蟒蛇`datetime.timedelta`，在大多数情况下可以互换。**`Timedelta.floor()``pandas.Timedelta`中的**方法用于将新的时间增量重置为该分辨率。

> **语法:**时间增量下限()
> 
> **参数:**
> **频率:**表示地板分辨率的频率字符串
> 
> **退货:**新地板时间增量。

**代码#1:**

```py
# importing pandas as pd 
import pandas as pd 
import datetime

# Create the Timedelta object 
td = pd.Timedelta(5.05, unit ='s')

# Print the Timedelta object 

print(td.floor('S'))
```

**输出:**

```py
 0 days 00:00:05
```

**代码#2:**

```py
# importing pandas as pd 
import pandas as pd 
import datetime

# Create the Timedelta object 
td = pd.Timedelta(13.25, unit ='h')

# Print the Timedelta object 

print(td.floor('H'))
```

**输出:**

```py
0 days 13:00:00
```

**代码#3:**

```py
# importing pandas as pd 
import pandas as pd 
from datetime import datetime

# Create the Timedelta object 
td = pd.Timedelta('7 days 15 hours')

# Print the Timedelta object 

print(td.floor('D'))
```

**输出:**

```py
7 days 00:00:00
```
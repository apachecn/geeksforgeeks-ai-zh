# python | pandas time delta . ceil()

> 哎哎哎:1230【https://www . geeksforgeeks . org/python 熊猫-timedelta-ceil/

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。Pandas 就是其中之一，它让数据的导入和分析变得更加容易。

时间增量是`datetime.timedelta`的一个子类，并且以类似的方式表现。它相当于熊猫的蟒蛇`datetime.timedelta`，在大多数情况下可以互换。**`Timedelta.ceil()``pandas.Timedelta`中的**方法用于将新的时间增量返回到该分辨率。

> **语法:** Timedelta.ceil()
> 
> **参数:**
> **freq :** 表示天花板分辨率的 freq 字符串
> 
> **返回:**新接收的时间增量。

**代码#1:**

```
# importing pandas as pd 
import pandas as pd 
import datetime

# Create the Timedelta object 
td = pd.Timedelta(5.05, unit ='s')

# Print the Timedelta object 

print(td.ceil('S'))
```

**输出:**

```
0 days 00:00:06
```

**代码#2:**

```
# importing pandas as pd 
import pandas as pd 
import datetime

# Create the Timedelta object 
td = pd.Timedelta(13.25, unit ='h')

# Print the Timedelta object 

print(td.ceil('H'))
```

**输出:**

```
 0 days 14:00:00
```

**代码#3:**

```
# importing pandas as pd 
import pandas as pd 
from datetime import datetime

# Create the Timedelta object 
td = pd.Timedelta('7 days 15 hours')

# Print the Timedelta object 

print(td.ceil('D'))
```

**输出:**

```
 8 days 00:00:00
```
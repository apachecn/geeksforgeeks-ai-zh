# Python |熊猫时间增量指数. dttype

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-pandas-time delta index-dtype/

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**TimedeltaIndex.dtype**`属性返回时间增量索引对象的数据类型。

> **语法:t1】timedeletendex . dtype**
> 
> **返回:**dttype

**示例#1:** 使用`TimedeltaIndex.dtype`属性查找给定时间增量索引对象的数据类型。

```py
# importing pandas as pd
import pandas as pd

# Create the TimedeltaIndex object
tidx = pd.TimedeltaIndex(data =['1 days 02:00:00', 
                        '1 days 06:05:01.000030'])

# Print the TimedeltaIndex
print(tidx)
```

**输出:**
![](img/866c50f3d2f4d26644ad715e5c073707.png)
现在我们要找出给定 TimedeltaIndex 对象的数据类型。

```py
# return the data type of the 
# values in the given object
tidx.dtype
```

**输出:**
![](img/e62adc6f3bde1004a59f88d4469f709b.png)
正如我们在输出中看到的，`TimedeltaIndex.dtype`已经返回了 tidx 对象中值的底层数据类型。

**示例 2:** 使用`TimedeltaIndex.dtype`属性查找给定 TimedeltaIndex 对象的数据类型。

```py
# importing pandas as pd
import pandas as pd

# Create the TimedeltaIndex object
tidx = pd.TimedeltaIndex(data =['-1 days 2 min 3us', '1 days 06:05:01.000030',
                                                '-1 days + 23:59:59.999999'])

# Print the TimedeltaIndex
print(tidx)
```

**输出:**
![](img/f5468003d01cf5883b597cb323de040e.png)

现在我们想找出给定的时间增量索引对象的数据类型。

```py
# return the data type of the
#  values in the given object
tidx.dtype
```

**输出:**
![](img/e62adc6f3bde1004a59f88d4469f709b.png)
正如我们在输出中看到的，`TimedeltaIndex.dtype`已经返回了 tidx 对象中值的底层数据类型。
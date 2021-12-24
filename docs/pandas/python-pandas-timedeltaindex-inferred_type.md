# 蟒蛇|熊猫时间增量索引.推断 _ 类型

> 原文:[https://www . geesforgeks . org/python-pandas-time deltaindex-explicated _ type/](https://www.geeksforgeeks.org/python-pandas-timedeltaindex-inferred_type/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

Pandas `**TimedeltaIndex.inferred_type**`属性返回应用它的对象的推断类型。

> **语法:**时间增量索引.推断 _ 类型
> 
> **返回:**推断 _ 类型

**示例#1:** 使用`TimedeltaIndex.inferred_type`属性推断时间增量索引对象的类型。

```
# importing pandas as pd
import pandas as pd

# Create the TimedeltaIndex object
tidx = pd.TimedeltaIndex(data =['1 days 02:00:00', 
                   '1 days 06:05:01.000030', None])

# Print the TimedeltaIndex
print(tidx)
```

**输出:**
![](img/62968e4e534bb4dad3065558648909c8.png)

现在我们将猜测给定时间增量索引对象的类型。

```
# return the inferred type of the tidx object
tidx.inferred_type
```

**输出:**
![](img/953fe162451685c7d25e528725accd9b.png)
正如我们在输出中看到的，`TimedeltaIndex.inferred_type`属性已经为 tidx 对象返回了‘time delta 64’类型。

**示例#2:** 使用`TimedeltaIndex.inferred_type`属性推断 TimedeltaIndex 对象的类型。

```
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

现在我们将猜测给定时间增量索引对象的类型。

```
# return the inferred type of the tidx object
tidx.inferred_type
```

**输出:**
![](img/953fe162451685c7d25e528725accd9b.png)
正如我们在输出中看到的，`TimedeltaIndex.inferred_type`属性已经为 tidx 对象返回了‘time delta 64’类型。
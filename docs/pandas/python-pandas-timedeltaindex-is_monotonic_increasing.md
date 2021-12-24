# Python | Pandas time deltaindex . is _ 单调 _ 递增

> 原文:[https://www . geesforgeks . org/python-pandas-time deltaindex-is _ 单调 _ 递增/](https://www.geeksforgeeks.org/python-pandas-timedeltaindex-is_monotonic_increasing/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

如果索引值单调递增，熊猫 `**TimedeltaIndex.is_monotonic_increasing**`属性返回`True`。即使值相等，它也会返回`True`。

> **语法:**时间增量索引. is _ 单调 _ 递增
> 
> **返回:**布尔值

**示例#1:** 使用`TimedeltaIndex.is_monotonic_increasing`属性检查时间增量索引对象是否单调增加。

```py
# importing pandas as pd
import pandas as pd

# Create the TimedeltaIndex object
tidx = pd.TimedeltaIndex(start ='1 days 02:00:00', periods = 5, freq ='T')

# Print the TimedeltaIndex
print(tidx)
```

**输出:**
![](img/2edf6147730bd28456b4797fe3d2f5d9.png)

现在我们将检查时间增量索引对象是否单调增加。

```py
# check if tidx is monotonic increasing or not
tidx.is_monotonic_increasing
```

**输出:**
![](img/5507be7e27f61a843c1cf5dc48d34011.png)
正如我们在输出中看到的，`TimedeltaIndex.is_monotonic_increasing`属性已经返回了`True`，表示 tidx 对象中的值是单调递增的。

**示例 2:** 使用`TimedeltaIndex.is_monotonic_increasing`属性检查时间增量索引对象是否单调增加。

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

现在我们将检查时间增量索引对象是否单调增加。

```py
# check if tidx is monotonic increasing or not
tidx.is_monotonic_increasing
```

**输出:**
![](img/3e5222c679e32dcaf3e86c0e0d0ef4ca.png)
正如我们在输出中看到的，`TimedeltaIndex.is_monotonic_increasing`属性已经返回了`False`，表明 tidx 对象中的值不是单调递增的。
# Python | Pandas time delta index . symmetric _ difference()

> 原文:[https://www . geesforgeks . org/python-pandas-time delta index-symmetric _ difference/](https://www.geeksforgeeks.org/python-pandas-timedeltaindex-symmetric_difference/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫**time delta Index . symmetric _ difference()**函数计算两个 Index 对象的对称差。如果排序是可能的，它将被排序。对于给定的一对 TimedeltaIndex 对象 idx1 和 idx2，symmetric_difference 包含出现在 idx1 或 idx2 中的元素，但不能同时出现在两者中。相当于 idx1.difference(idx2)或 idx2.difference(idx1)创建的索引，但删除了重复项。

> **语法:**time delta Index . symmetric _ difference(other，result_name=None)
> **参数:**
> **other :** Index 或类似数组的
> **result _ name:**str
> **Return:**symmetric _ difference:Index

**示例#1:** 使用 TimedeltaIndex . symmetric _ difference()函数求两个 time delta index 对象的对称差。

## 蟒蛇 3

```py
# importing pandas as pd
import pandas as pd

# Create the first TimedeltaIndex object
tidx1 = pd.TimedeltaIndex(data =['06:05:01.000030', '+23:59:59.999999',
                         '22 day 2 min 3us 10ns', '+23:29:59.999999',
                         '+12:19:59.999999'])

# Create the second TimedeltaIndex object
tidx2 = pd.TimedeltaIndex(data =['09:11:18.000030', '+23:59:59.999999',
                         '9 day 18 min 3us ', '+23:29:59.999999',
                         '+12:19:59.999999'])

# Print the first TimedeltaIndex object
print(tidx1)

# Print the second TimedeltaIndex object
print(tidx2)
```

**输出:**

![](img/708240dfe9aedf867ac5c12c98b02393.png)

![](img/6f6cc0167371df9ee775333327837506.png)

现在我们将使用 timedeltaindex . symmetric _ difference()函数来找到对称差。

## 蟒蛇 3

```py
# find the symmetric difference
tidx1.symmetric_difference(tidx2)
```

**输出:**

![](img/0d3daa28d7b8f23c7bde84dc1d304627.png)

正如我们在输出中看到的，timedeltaindex . symmetric _ difference()函数返回了一个新的对象，该对象只包含两个对象不共有的元素。

**例 2:** 使用 TimedeltaIndex . symmetric _ difference()函数求两个 TimedeltaIndex 对象的对称差。

## 蟒蛇 3

```py
# importing pandas as pd
import pandas as pd

# Create the first TimedeltaIndex object
tidx1 = pd.TimedeltaIndex(start ='1 days 02:00:12.001124',
                          periods = 5, freq ='D', name ='Koala')

# Create the second TimedeltaIndex object
tidx2 = pd.TimedeltaIndex(start ='3 days 02:00:12.001124',
                          periods = 5, freq ='D', name ='Koala')

# Print the first TimedeltaIndex object
print(tidx1)

# Print the second TimedeltaIndex object
print(tidx2)
```

**输出:**

![](img/4b1498214e3c6e8c3ca75b1dc780223c.png)

![](img/6a341c39cdcb2a0d568cc9cae555ccaf.png)

现在我们将使用 timedeltaindex . symmetric _ difference()函数来找到对称差。

## 蟒蛇 3

```py
# find the symmetric difference
tidx1.symmetric_difference(tidx2)
```

**输出:**

![](img/34baae75280dd3d015e51d84377f691e.png)

正如我们在输出中看到的，timedeltaindex . symmetric _ difference()函数返回了一个新的对象，该对象只包含两个对象不共有的元素。
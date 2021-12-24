# 从数组

创建熊猫系列

> 原文:[https://www . geeksforgeeks . org/create-a-pandas-series-from-array/](https://www.geeksforgeeks.org/create-a-pandas-series-from-array/)

**[熊猫系列](https://www.geeksforgeeks.org/python-pandas-series/)** 是一维标签数组，能够保存任何数据类型(整数、字符串、浮点数、Python 对象等)。).必须记住，与 Python 列表不同，系列总是包含相同类型的数据。

让我们看看如何从数组中创建熊猫系列。

**方法#1:** 从没有索引的数组创建一个序列。

在这种情况下，由于没有传递索引，因此默认情况下，索引将是`range(n)`，其中 *n* 是数组长度。

```
# importing Pandas & numpy
import pandas as pd
import numpy as np

# numpy array
data = np.array(['a', 'b', 'c', 'd', 'e'])

# creating series
s = pd.Series(data)
print(s)
```

**Output:**

```
0    a
1    b
2    c
3    d
4    e
dtype: object

```

**方法 2:** 用带索引的数组创建一个数列。

在这种情况下，我们将把索引作为参数传递给构造函数。

```
# importing Pandas & numpy
import pandas as pd
import numpy as np

# numpy array
data = np.array(['a', 'b', 'c', 'd', 'e'])

# creating series
s = pd.Series(data, index =[1000, 1001, 1002, 1003, 1004])
print(s)
```

**Output:**

```
1000    a
1001    b
1002    c
1003    d
1004    e
dtype: object

```
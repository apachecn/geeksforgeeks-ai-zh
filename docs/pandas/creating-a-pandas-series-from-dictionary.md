# 从字典中创建熊猫系列

> 原文:[https://www . geesforgeks . org/creating-a-pandas-series-from-dictionary/](https://www.geeksforgeeks.org/creating-a-pandas-series-from-dictionary/)

A **`Series`** 是一个一维标注数组，能够保存任意数据类型(整数、字符串、浮点数、Python 对象等)。).必须记住，与 Python 列表不同，系列总是包含相同类型的数据。

让我们看看如何从字典中创建熊猫系列。

### 使用无`index` 参数的`Series()`方法。

在这种情况下，字典键按照排序的顺序来构造索引。

**代码#1 :** 字典键按排序顺序给出。

```py
# import the pandas lib as pd
import pandas as pd

# create a dictionary
dictionary = {'A' : 10, 'B' : 20, 'C' : 30}

# create a series
series = pd.Series(dictionary)

print(series)
```

**Output:**

```py
A    10
B    20
C    30
dtype: int64

```

**代码#2 :** 字典键按未排序的顺序给出。

```py
# import the pandas lib as pd
import pandas as pd

# create a dictionary
dictionary = {'D' : 10, 'B' : 20, 'C' : 30}

# create a series
series = pd.Series(dictionary)

print(series)
```

**Output:**

```py
B    20
C    30
D    10
dtype: int64

```

### 使用带`index`参数的`Series()`方法。

在这种情况下，将分配与索引中的标签相对应的数据值。

**代码#1 :** 索引列表的长度与字典中存在的键的数量相同。

```py
# import the pandas lib as pd
import pandas as pd

# create a dictionary
dictionary = {'A' : 50, 'B' : 10, 'C' : 80}

# create a series
series = pd.Series(dictionary, index =['B', 'C', 'A'])

print(series)
```

**Output:**

```py
B    10
C    80
A    50
dtype: int64

```

**代码#2 :** 传递的索引列表的长度大于字典中存在的键的数量在这种情况下，索引顺序保持不变，缺少的元素用 NaN(不是数字)填充。

```py
# import the pandas lib as pd
import pandas as pd

# create a dictionary
dictionary = {'A' : 50, 'B' : 10, 'C' : 80}

# create a series
series = pd.Series(dictionary, index =['B', 'C', 'D', 'A'])

print(series)
```

**Output:**

```py
B    10
C    80
D   NaN
A    50
dtype: float64

```
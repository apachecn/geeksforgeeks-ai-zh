# Python | Pandas index . value _ counts()

> 原文:[https://www . geesforgeks . org/python-pandas-index-value _ counts/](https://www.geeksforgeeks.org/python-pandas-index-value_counts/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。
熊猫 **Index.value_counts()** 函数返回包含唯一值计数的对象。结果对象将按降序排列，因此第一个元素是最常出现的元素。默认情况下不包括数值。

> **语法:**index . value _ counts(normalize =False，sort=True，升序= False，bins = None，dropna=True)
> **参数:**
> **normalize :** 如果为 True，则返回的对象将包含唯一值的相对频率。
> **排序:**按值排序
> **升序:**按升序排序
> **条块:**与其对值进行计数，不如将它们分组到半开条块中，这是 pd.cut 的一种便利，只适用于数字数据
> **dropna :** 不包括 NaN 的计数。
> T21】返回:计数:系列

**示例#1:** 使用 Index.value_counts()函数计算给定索引中唯一值的数量。

## 蟒蛇 3

```
# importing pandas as pd
import pandas as pd

# Creating the index
idx = pd.Index(['Harry', 'Mike', 'Arther', 'Nick',
                'Harry', 'Arther'], name ='Student')

# Print the Index
print(idx)
```

**输出:**

```
Index(['Harry', 'Mike', 'Arther', 'Nick', 'Harry', 'Arther'], dtype='object', name='Student')
```

让我们找出索引中所有唯一值的计数。

## 蟒蛇 3

```
# find the count of unique values in the index
idx.value_counts()
```

**输出:**

```
Harry     2
Arther    2
Nick      1
Mike      1
Name: Student, dtype: int64
```

该函数已返回给定索引中所有唯一值的计数。请注意，函数返回的对象包含以降序排列的值。

**示例#2:** 使用 Index.value_counts()函数查找给定索引中所有唯一值的计数。

## 蟒蛇 3

```
# importing pandas as pd
import pandas as pd

# Creating the index
idx = pd.Index([21, 10, 30, 40, 50, 10, 50])

# Print the Index
print(idx)
```

**输出:**

```
Int64Index([21, 10, 30, 40, 50, 10, 50], dtype='int64')
```

让我们计算索引中所有唯一值的出现次数。

## 蟒蛇 3

```
# for finding the count of all
# unique values in the index.
idx.value_counts()
```

**输出:**

```
10    2
50    2
30    1
21    1
40    1
dtype: int64
```

该函数返回了索引中所有唯一值的计数。
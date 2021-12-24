# 蟒蛇|熊猫系列. append()

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-append/](https://www.geeksforgeeks.org/python-pandas-series-append/)

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

熊猫 `**Series.append()**`功能用于连接两个或多个系列对象。

> **语法:** Series.append(to_append，ignore_index=False，verify_integrity=False)
> 
> **参数:**
> **至 _ 追加:**系列或系列的列表/元组
> **忽略 _ 索引:**如果为真，则不要使用索引标签。
> **验证 _ 完整性:**如果为真，则在创建重复索引时引发异常
> 
> **返回:**附加:系列

**示例#1:** 使用`Series.append()`函数将传递的序列对象追加到该序列对象的末尾。

```py
# importing pandas as pd
import pandas as pd

# Creating the first Series
sr1 = pd.Series(['New York', 'Chicago', 'Toronto', 'Lisbon', 'Rio'])

# Create the first Index
index_1 = ['City 1', 'City 2', 'City 3', 'City 4', 'City 5'] 

# set the index of first series
sr1.index = index_1

# Creating the second Series
sr2 = pd.Series(['Chicage', 'Shanghai', 'Beijing', 'Jakarta', 'Seoul'])

# Create the second Index
index_2 = ['City 6', 'City 7', 'City 8', 'City 9', 'City 10'] 

# set the index of second series
sr2.index = index_2

# Print the first series
print(sr1)

# Print the second series
print(sr2)
```

**输出:**

```py
City 1    New York
City 2     Chicago
City 3     Toronto
City 4      Lisbon
City 5         Rio
dtype: object

City 6      Chicage
City 7     Shanghai
City 8      Beijing
City 9      Jakarta
City 10       Seoul
dtype: object
```

现在我们使用`Series.append()`函数在 sr1 系列的末尾追加 sr2。

```py
# append sr2 at the end of sr1
result = sr1.append(sr2)

# Print the result
print(result)
```

**输出:**

```py
City 1     New York
City 2      Chicago
City 3      Toronto
City 4       Lisbon
City 5          Rio
City 6      Chicage
City 7     Shanghai
City 8      Beijing
City 9      Jakarta
City 10       Seoul
dtype: object
```

正如我们在输出中看到的那样，`Series.append()`函数已经成功地在 sr1 对象的末尾追加了 sr2 对象。

**示例 2:** 使用`Series.append()`函数将传递的系列对象追加到该系列对象的末尾。忽略两个系列对象的原始索引。

```py
# importing pandas as pd
import pandas as pd

# Creating the first Series
sr1 = pd.Series(['New York', 'Chicago', 'Toronto', 'Lisbon', 'Rio'])

# Create the first Index
index_1 = ['City 1', 'City 2', 'City 3', 'City 4', 'City 5'] 

# set the index of first series
sr1.index = index_1

# Creating the second Series
sr2 = pd.Series(['Chicage', 'Shanghai', 'Beijing', 'Jakarta', 'Seoul'])

# Create the second Index
index_2 = ['City 6', 'City 7', 'City 8', 'City 9', 'City 10'] 

# set the index of second series
sr2.index = index_2

# Print the first series
print(sr1)

# Print the second series
print(sr2)
```

**输出:**

```py
City 1    New York
City 2     Chicago
City 3     Toronto
City 4      Lisbon
City 5         Rio
dtype: object

City 6      Chicage
City 7     Shanghai
City 8      Beijing
City 9      Jakarta
City 10       Seoul
dtype: object
```

现在我们使用`Series.append()`函数在 sr1 系列的末尾追加 sr2。我们将忽略给定序列对象的索引。

```py
# append sr2 at the end of sr1
# ignore the index
result = sr1.append(sr2, ignore_index = True)

# Print the result
print(result)
```

**输出:**

```py
0    New York
1     Chicago
2     Toronto
3      Lisbon
4         Rio
5     Chicage
6    Shanghai
7     Beijing
8     Jakarta
9       Seoul
dtype: object
```

正如我们在输出中看到的那样，`Series.append()`函数已经成功地在 sr1 对象的末尾追加了 sr2 对象，并且它还忽略了索引。
# 合并两个条件复杂的熊猫数据帧

> 原文:[https://www . geesforgeks . org/merge-two-pandas-data frames-with-complex-conditions/](https://www.geeksforgeeks.org/merge-two-pandas-dataframes-with-complex-conditions/)

在本文中，我们将讨论如何在一些复杂的条件下合并两个熊猫数据帧。熊猫中的数据帧可以使用 [**pandas.merge()**](https://www.geeksforgeeks.org/python-pandas-merging-joining-and-concatenating/) 方法进行合并。

> **语法:**
> 
> *熊猫. merge(参数)*
> 
> ***返回:**两个合并对象的数据帧。*

在处理数据集时，可能需要合并具有一些复杂条件的两个数据框，以下是合并具有一些复杂条件的两个数据框的一些示例。

**例 1 :**

使用 merge()函数合并两个数据帧，参数作为两个数据帧。

## 蟒蛇 3

```
# importing pandas as pd
import pandas as pd

# creating dataframes
df1 = pd.DataFrame({'ID': [1, 2, 3, 4], 
                    'Name': ['John', 'Tom', 'Simon', 'Jose']})

df2 = pd.DataFrame({'ID': [1, 2, 3, 5], 
                    'Class': ['Second', 'Third', 'Fifth', 'Fourth']})

# merging df1 and df2 with merge function
df = pd.merge(df1, df2)
print(df)
```

**输出:**

![](img/39246b420d40a74751793c614ae693bc.png)

**例 2 :**

使用 merge()函数在数据框的某个指定列名上合并两个数据框。

## 蟒蛇 3

```
# importing pandas as pd
import pandas as pd

# creating dataframes
df1 = pd.DataFrame({'Name': ['John', 'Tom', 'Simon', 'Jose'],
                    'Age': [5, 6, 4, 5]})

df2 = pd.DataFrame({'Name': ['John', 'Tom', 'Jose'],
                    'Class': ['Second', 'Third', 'Fifth']})

# merging df1 and df2 with merge function 
# with the common column as Name
df = pd.merge(df1, df2, on='Name')
print(df)
```
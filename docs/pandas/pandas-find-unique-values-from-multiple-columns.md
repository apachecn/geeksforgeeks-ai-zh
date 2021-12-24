# 熊猫–从多列中找到唯一值

> 原文:[https://www . geesforgeks . org/pandas-find-unique-values-from-multi-columns/](https://www.geeksforgeeks.org/pandas-find-unique-values-from-multiple-columns/)

**先决条件:**T2】熊猫

在本文中，我们将讨论从熊猫数据帧的多列中获取唯一值的各种方法。

**方法 1:** 采用熊猫[独特()](https://www.geeksforgeeks.org/python-pandas-series-unique/)和[多卡()](https://www.geeksforgeeks.org/pandas-concat-function-in-python/)方法

Pandas 系列又名 columns 有一个独特的()方法，它只从一个列中过滤出唯一的值。第一个输出只显示唯一的名字。我们可以使用 pandas **concat()** 方法扩展这个方法，将所有需要的列连接成一个单独的列，然后找到结果列的唯一性。

## 蟒 3

```
import pandas as pd
import numpy as np

# Creating a custom dataframe.
df = pd.DataFrame({'FirstName': ['Arun', 'Navneet', 'Shilpa',
                                 'Prateek', 'Pyare', 'Prateek'],

                   'LastName': ['Singh', 'Yadav', 'Yadav', 'Shukla',
                                'Lal', 'Mishra'],

                   'Age': [26, 25, 25, 27, 28, 30]})

# To get unique values in 1 series/column
print(f"Unique FN: {df['FirstName'].unique()}")

# Extending the idea from 1 column to multiple columns
print(f"Unique Values from 3 Columns:\
{pd.concat([df['FirstName'],df['LastName'],df['Age']]).unique()}")
```

**输出:**

> 唯一 FN:[' Arun ' ' Navneet ' ' Shilpa ' ' Prateek ' ' Pyare ']
> 
> 来自 3 列的唯一值:[' Arun ' ' Navneet ' ' Shilpa ' ' Prateek ' ' Pyare ' ' Singh ' ' Yadav ' ' Shukla '
> 
> 【Lal ' ' Mishra ' 26 25 27 28 30】

**方法二:**使用 [Numpy.unique()](https://www.geeksforgeeks.org/python-numpy-np-unique-method/) 方法

借助于 np.unique()方法，我们可以从一个在 np.unique()方法中作为参数给定的数组中获得唯一的值。

**注意:**这种方法有一个限制，即我们不能将字符串和数字列组合在一起<u>、</u>因此，如果出现需要将不同数据类型的列组合在一起的情况，那么就选择方法 1。

## 蟒 3

```
import pandas as pd
import numpy as np

# Creating a custom dataframe.
df = pd.DataFrame({'FirstName': ['Arun', 'Navneet', 'Shilpa',
                                 'Prateek', 'Pyare', 'Prateek'],

                   'LastName': ['Singh', 'Yadav', 'Yadav', 'Shukla',
                                'Lal', 'Mishra'],

                   'Age': [26, 25, 25, 27, 28, 30]})

print(np.unique(df[['LastName', 'FirstName']].values))

# Will throw error as Age is numerical datatype
# and LastName is str
# print(np.unique(df[['LastName','Age']].values))
```

**输出:**

> 【“阿伦”“拉尔”“米什拉”“纳夫尼特”“普拉泰克”“皮瓦尔”“希尔帕”“舒克拉”
> 
> 【辛格”“亚达夫】】

**方法三:**使用 Python 中的[集](https://www.geeksforgeeks.org/sets-in-python/)

集合具有仅包含唯一值的属性，因此我们将单个系列转换为集合对象，然后取它们的集合并集。与方法 2 不同，这也适用于所有数据类型组合。

## 蟒 3

```
import pandas as pd
import numpy as np

# Creating a custom dataframe.
df = pd.DataFrame({'FirstName': ['Arun', 'Navneet', 'Shilpa',
                                 'Prateek', 'Pyare', 'Prateek'],

                   'LastName': ['Singh', 'Yadav', 'Yadav', 'Shukla',
                                'Lal', 'Mishra'],

                   'Age': [26, 25, 25, 27, 28, 30]})

# Typecasting pandas series into set and then
# taking set union (|)
print(set(df.FirstName) | set(df.LastName) | set(df.Age))
```

**输出:**

> {'Singh '，' Pyare '，' Mishra '，27，' Navneet '，' Arun '，' Lal '，' Shukla '，30，25，26，' Yadav '，28，' Shilpa '，' Prateek'}
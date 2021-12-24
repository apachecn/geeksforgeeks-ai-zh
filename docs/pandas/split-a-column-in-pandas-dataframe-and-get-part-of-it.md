# 在熊猫数据框中分割一列并获得其中的一部分

> 原文:[https://www . geesforgeks . org/split-a-column-in-pandas-data frame-and-get-part-it/](https://www.geeksforgeeks.org/split-a-column-in-pandas-dataframe-and-get-part-of-it/)

当 Dataframe 中任何列的一部分很重要并且需要将其分离时，我们可以根据需求拆分一个列。

我们可以用熊猫*。str* 访问器，它对 Series 和 Dataframes 进行快速矢量化字符串操作，并返回一个字符串对象。Pandas str 访问器有许多有用的方法，其中之一是`str.split`，它可以与 split 一起使用来获取字符串的所需部分。要获取字符串的第 *n <sup>th</sup>* 部分，首先通过分隔符分割列，并在返回的对象上再次应用*str【n-1】*，即`Dataframe.columnName.str.split(" ").str[n-1]`。

我们通过例子来说明一下。

**代码#1:** 打印分割列的数据对象。

```
import pandas as pd
import numpy as np
df = pd.DataFrame({'Geek_ID':['Geek1_id', 'Geek2_id', 'Geek3_id', 
                                         'Geek4_id', 'Geek5_id'],
                'Geek_A': [1, 1, 3, 2, 4],
                'Geek_B': [1, 2, 3, 4, 6],
                'Geek_R': np.random.randn(5)})

# Geek_A  Geek_B   Geek_ID    Geek_R
# 0       1       1  Geek1_id    random number
# 1       1       2  Geek2_id    random number
# 2       3       3  Geek3_id    random number
# 3       2       4  Geek4_id    random number
# 4       4       6  Geek5_id    random number

print(df.Geek_ID.str.split('_').str[0])
```

**Output:**

```
0    Geek1
1    Geek2
2    Geek3
3    Geek4
4    Geek5
dtype: object

```

**代码#2:** 打印返回数据对象列表。

```
import pandas as pd
import numpy as np
df = pd.DataFrame({'Geek_ID':['Geek1_id', 'Geek2_id', 'Geek3_id',
                                         'Geek4_id', 'Geek5_id'],
                'Geek_A': [1, 1, 3, 2, 4],
                'Geek_B': [1, 2, 3, 4, 6],
                'Geek_R': np.random.randn(5)})

# Geek_A  Geek_B   Geek_ID    Geek_R
# 0       1       1  Geek1_id    random number
# 1       1       2  Geek2_id    random number
# 2       3       3  Geek3_id    random number
# 3       2       4  Geek4_id    random number
# 4       4       6  Geek5_id    random number

print(df.Geek_ID.str.split('_').str[0].tolist())
```

**Output:**

```
['Geek1', 'Geek2', 'Geek3', 'Geek4', 'Geek5']

```

**代码#3:** 打印元素列表。

```
import pandas as pd
import numpy as np

df = pd.DataFrame({'Geek_ID':['Geek1_id', 'Geek2_id', 'Geek3_id',
                                         'Geek4_id', 'Geek5_id'],
                'Geek_A': [1, 1, 3, 2, 4],
                'Geek_B': [1, 2, 3, 4, 6],
                'Geek_R': np.random.randn(5)})

# Geek_A  Geek_B   Geek_ID    Geek_R
# 0       1       1  Geek1_id    random number
# 1       1       2  Geek2_id    random number
# 2       3       3  Geek3_id    random number
# 3       2       4  Geek4_id    random number
# 4       4       6  Geek5_id    random number

print(df.Geek_ID.str.split('_').str[1].tolist())
```

**Output:**

```
['id', 'id', 'id', 'id', 'id']

```
# 使用字典在熊猫数据框中添加新列

> 原文:[https://www . geesforgeks . org/add-a-new-in-column-pands-data-frame-use-a-dictionary/](https://www.geeksforgeeks.org/add-a-new-column-in-pandas-data-frame-using-a-dictionary/)

Pandas 基本上是 Python 中用于数据分析和操作的库。要在数据框中添加新列，我们有多种方法。但是在这篇文章中，我们正在讨论使用[字典](https://www.geeksforgeeks.org/python-dictionary/)添加一个新的专栏。

**举个例子吧！**

```
# Python program to illustrate
# Add a new column  in Pandas 

# Importing the pandas Library
import pandas as pd

# creating a data frame with some data values.
data_frame = pd.DataFrame([[i] for i in range(7)], columns =['data'])

print (data_frame)
```

**输出:**

```
  data 
0  0
1  1
2  2
3  3
4  4
5  5
6  6

```

现在使用上面写的方法，让我们尝试向它添加一个新的列。让我们添加名为**“New _ data _ 1”**的新列。
**地图功能:**通过给名为**【数据】**的列赋予获取周名的功能，增加列“new_data_1”。调用 map 并传递 dict，这将执行查找并返回该键的关联值。

让我们介绍以字典形式键入的可变周数据，其中包括一周中的天数。

```
# Python program to illustrate
# Add a new column  in Pandas 
# Data Frame Using a Dictionary

import pandas as pd

data_frame = pd.DataFrame([[i] for i in range(7)], columns =['data'])

# Introducing weeks as dictionary
weeks = {0:'Sunday', 1:'Monday', 2:'Tuesday', 3:'Wednesday', 
4:'Thursday', 5:'Friday', 6:'Saturday'}

# Mapping the dictionary keys to the data frame.
data_frame['new_data_1'] = data_frame['data'].map(weeks)
print (data_frame)
```

**输出:**

```
  data  new_data_1
0  0  Sunday
1  1  Monday
2  2  Tuesday
3  3  Wednesday
4  4  Thursday
5  5  Friday
6  6  Saturday

```

并且，我们已经成功添加了一个专栏(周日，周一……。)结尾。
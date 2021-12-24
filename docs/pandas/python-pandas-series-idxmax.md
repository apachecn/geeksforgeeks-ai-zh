# Python | Pandas series . idxmax()

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-idxmax/](https://www.geeksforgeeks.org/python-pandas-series-idxmax/)

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

熊猫 `**Series.idxmax()**`功能返回最大值的行标签。如果多个值等于最大值，则返回具有该值的第一行标签。

> **语法:** Series.idxmax(axis=0，skipna=True，*args，**kwargs)
> 
> **参数:**
> **skipna :** 排除 NA/null 值。如果整个系列都是 NA，结果就是 NA。
> **轴:**用于与 DataFrame.idxmax 兼容。冗余用于系列上的应用。
> 
> **返回:** idxmax:最大值的索引。

**示例#1:** 使用`Series.idxmax()`函数查找给定序列对象中最大值对应的索引标签。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series([10, 25, 3, 25, 24, 6])

# Create the Index
index_ = ['Coca Cola', 'Sprite', 'Coke', 'Fanta', 'Dew', 'ThumbsUp']

# set the index
sr.index = index_

# Print the series
print(sr)
```

**输出:**

![](img/1f53af828e1a9600b255c9201272ff8a.png)

现在我们将使用`Series.idxmax()`函数来查找序列中最大值对应的索引标签。

```py
# return index label of the 
# maximum value in the series
result = sr.idxmax()

# Print the result
print(result)
```

**输出:**

![](img/ae38990ed830e726dc9487ae82bf18d0.png)

我们可以在输出中看到，`Series.idxmax()`函数已经返回了给定序列对象中最大元素的索引标签。

**示例#2 :** 使用`Series.idxmax()`函数查找给定序列对象中最大值对应的索引标签。

```py
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series([11, 21, 8, 18, 65, 84, 32, 10, 5, 24, 32])

# Create the Index
index_ = pd.date_range('2010-10-09', periods = 11, freq ='M')

# set the index
sr.index = index_

# Print the series
print(sr)
```

**输出:**
![](img/229bdc336ad3db176b98acf5dad7297f.png)

现在我们将使用`Series.idxmax()`函数来查找序列中最大值对应的索引标签。

```py
# return index label of the 
# maximum value in the series
result = sr.idxmax()

# Print the result
print(result)
```

**输出:**
![](img/a43447638488bfe984de0d55638123b4.png)
正如我们在输出中看到的，`Series.idxmax()`函数已经返回了给定序列对象中最大元素的索引标签。
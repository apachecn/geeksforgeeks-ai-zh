# 蟒蛇|熊猫系列. iat

> 原文:[https://www.geeksforgeeks.org/python-pandas-series-iat/](https://www.geeksforgeeks.org/python-pandas-series-iat/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫系列是带有轴标签的一维数组。标签不必是唯一的，但必须是可散列的类型。该对象支持基于整数和基于标签的索引，并提供了一系列方法来执行涉及索引的操作。

熊猫 `**Series.iat**`属性通过整数位置访问行/列对的单个值。

> **语法:** Series.iat
> 
> **参数:**无
> 
> **返回:**指定位置的返回值

**示例#1:** 使用`Series.iat`属性返回给定序列对象在指定位置的值。

```
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series(['New York', 'Chicago', 'Toronto', 'Lisbon'])

# Creating the row axis labels
sr.index = ['City 1', 'City 2', 'City 3', 'City 4'] 

# Print the series
print(sr)
```

**输出:**

![](img/4b2772771d6fb5d72c2864e9efa9f66a.png)

现在我们将使用`Series.iat`属性返回位于第 0 个索引处的值。

```
# return the value at 0th index
sr.iat[0]
```

**输出:**

![](img/a929e70e76dff07f5fa0c53178b1314a.png)

正如我们在输出中看到的那样，`Series.iat`属性返回了“New York”，这是给定 Series 对象中第 0 个索引处的值。

**示例 2 :** 使用`Series.iat`属性返回给定系列对象在指定位置的值。

```
# importing pandas as pd
import pandas as pd

# Creating the Series
sr = pd.Series(['1/1/2018', '2/1/2018', '3/1/2018', '4/1/2018'])

# Creating the row axis labels
sr.index = ['Day 1', 'Day 2', 'Day 3', 'Day 4']

# Print the series
print(sr)
```

**输出:**
![](img/a519278b0c944bba68cf9df8e3566a3b.png)

现在我们将使用`Series.iat`属性返回位于第二个索引处的值。

```
# return the value at 2nd index
sr.iat[2]
```

**输出:**

![](img/06ac4cc8dbc068901629b8ea731bc037.png)
正如我们在输出中看到的，`Series.iat`属性返回了‘3/1/2018’，这是给定 Series 对象中第二个索引处的值。
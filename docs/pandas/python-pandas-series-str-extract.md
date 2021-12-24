# Python | Pandas series . str . extract()

> 原文:[https://www . geesforgeks . org/python-pandas-series-str-extract/](https://www.geeksforgeeks.org/python-pandas-series-str-extract/)

`Series.str`可用于以字符串形式访问系列的值，并对其应用多种方法。Pandas `**Series.str.extract()**`函数用于将正则表达式 pat 中的捕获组提取为数据帧中的列。对于系列中的每个主题字符串，从正则表达式的第一个匹配中提取组*轻拍*。

> **语法:** Series.str.extract(pat，flags=0，expand=True)
> 
> **参数:**
> **拍:**带捕捉组的正则表达式模式。
> **标志:** int，默认 0(无标志)
> **展开:**如果为真，返回每个捕获组一列的 DataFrame。
> 
> **返回:**数据帧或序列或索引

**示例#1:** 使用`Series.str.extract()`函数从给定序列对象的基础数据中的字符串中提取组。

```py
# importing pandas as pd
import pandas as pd

# importing re for regular expressions
import re

# Creating the Series
sr = pd.Series(['New_York', 'Lisbon', 'Tokyo', 'Paris', 'Munich'])

# Creating the index
idx = ['City 1', 'City 2', 'City 3', 'City 4', 'City 5']

# set the index
sr.index = idx

# Print the series
print(sr)
```

**输出:**

![](img/187196ebd47e4e626ce688b1f83ddc77.png)

现在我们将使用`Series.str.extract()`函数从给定序列对象中的字符串中提取组。

```py
# extract groups having a vowel followed by
# any character
result = sr.str.extract(pat = '([aeiou].)')

# print the result
print(result)
```

**输出:**

![](img/aa2c27d078a53360ff47846be5d36625.png)

正如我们在输出中看到的那样，`Series.str.extract()`函数返回了一个包含提取组的一列的数据帧。

**示例#2 :** 使用`Series.str.extract()`函数从给定序列对象的基础数据中的字符串中提取组。

```py
# importing pandas as pd
import pandas as pd

# importing re for regular expressions
import re

# Creating the Series
sr = pd.Series(['Mike', 'Alessa', 'Nick', 'Kim', 'Britney'])

# Creating the index
idx = ['Name 1', 'Name 2', 'Name 3', 'Name 4', 'Name 5']

# set the index
sr.index = idx

# Print the series
print(sr)
```

**输出:**

![](img/573740fe100637d27c1161cf4a288888.png)

现在我们将使用`Series.str.extract()`函数从给定序列对象中的字符串中提取组。

```py
# extract groups having any capital letter
# followed by 'i' and any other character
result = sr.str.extract(pat = '([A-Z]i.)')

# print the result
print(result)
```

**输出:**

![](img/0daa9909787587d31cffbdc96b4498d6.png)

正如我们在输出中看到的那样，`Series.str.extract()`函数返回了一个包含提取组的一列的数据帧。
# Python | Pandas series . str . rfind()

> 原文:[https://www . geesforgeks . org/python-pandas-series-str-rfind/](https://www.geeksforgeeks.org/python-pandas-series-str-rfind/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。
Pandas **str.rfind()** 方法用于从右侧搜索序列中出现的每个字符串中的子字符串。如果找到该字符串，它将返回其出现的最高索引。如果没有找到字符串，它将返回-1。
也可以传递起点和终点，在字符串的特定部分搜索传递的字符或子字符串。

> **语法:** Series.str.rfind(sub，start=0，end=None)
> **参数:**
> **sub:** 要在文本值中搜索的字符串或字符在 series
> **中开始:** int 值，搜索的起始点。默认值为 0，表示从字符串
> **开始到:** int 值结束，需要停止搜索的结束点。默认值为无。
> **返回类型:**子串出现索引位置最高的序列

要下载代码中使用的 CSV，点击这里的[。](https://media.geeksforgeeks.org/wp-content/uploads/nba.csv)
在下面的例子中，使用的数据框包含了一些 NBA 球员的数据。任何操作前的数据框图像附在下面。

![](img/c703b6e6ac40ae8a3fdeceb5ba3a4d4c.png)

**示例#1:** 查找单个字符
在此示例中，使用 str.rfind()方法从名称列的每个字符串的右侧搜索单个字符“r”。开始和结束参数保持默认值。返回的序列存储在一个新的列中，以便可以通过直接查看来比较索引。在应用此方法之前，使用。dropna()以避免错误。

## 蟒蛇 3

```py
# importing pandas module
import pandas as pd

# reading csv file from url
data = pd.read_csv("https://media.geeksforgeeks.org/wp-content/uploads/nba.csv")

# dropping null value columns to avoid errors
data.dropna(inplace = True)

# substring to be searched
sub ='r'

# creating and passing series to new column
data["Indexes"]= data["Name"].str.rfind(sub)

# display
data
```

**输出:**
如输出图像所示，“索引”列中索引的出现位置等于字符串中字符最后出现的位置。如果文本中不存在子字符串，则返回-1。

![](img/a2d873933a171e1e1eae08e851f57015.png)

**例 2:** 搜索子串(多个字符)
在本例中，将在数据框的名称列中搜索‘ey’子串。start 参数保持为 2，从第 3 个(索引位置 2)元素开始搜索。

## 蟒蛇 3

```py
# importing pandas module
import pandas as pd

# reading csv file from url
data = pd.read_csv("https://media.geeksforgeeks.org/wp-content/upload/nba.csv")

# dropping null value columns to avoid errors
data.dropna(inplace = True)

# substring to be searched
sub ='ey'

# start var
start = 2

# creating and passing series to new column
data["Indexes"]= data["Name"].str.rfind(sub, start)

# display
data
```

**输出:**
如输出图像所示，返回子串出现的最高或最后一个索引。

![](img/22ae89fc86e8bd8c6a51241b72a0c8d0.png)
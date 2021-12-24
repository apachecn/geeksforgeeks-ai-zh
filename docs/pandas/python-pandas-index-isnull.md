# Python | Pandas index . is null()

> 原文:[https://www.geeksforgeeks.org/python-pandas-index-isnull/](https://www.geeksforgeeks.org/python-pandas-index-isnull/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 `**Index.isnull()**`功能检测缺失值。它返回一个相同大小的布尔对象，指示值是否为“无”。数值，如无、数值。NaN 或 pd。NaT，映射到真值。其他一切都被映射到假值。空字符串“”或 numpy.inf 等字符不被视为 NA 值(除非您设置 pandas . options . mode . use _ INF _ as _ NA = True)。

> **语法:** Index.isnull()
> 
> **参数:**不取任何参数。
> 
> **返回:**一个布尔数组，表示我的值是否为 NA

**示例#1:** 使用`Index.isnull()`功能检查索引中的任何值是否为`NaN`值。

```py
# importing pandas as pd
import pandas as pd

# Creating the Index
idx = pd.Index(['Labrador', None, 'Beagle', 'Mastiff',
                   'Lhasa', None, 'Husky', 'Beagle'])
# Print the Index
idx
```

**输出:**
![](img/417efa48b93049a6a07a66e03064c56a.png)

现在我们检查索引中缺少的值。

```py
# checks for missing values.
idx.isnull()
```

**输出:**
![](img/e884ce9ccccbaca58587d1162885f7ae.png)
该函数返回一个数组对象，其大小与索引的大小相同。`True`值表示索引标签丢失，`False`值表示索引标签存在。

**示例 2:** 使用`Index.isnull()`函数检查缺失的日期时间索引是否被视为`NaN`值。

```py
# importing pandas as pd
import pandas as pd

# Creating the Datetime Index
idx = pd.DatetimeIndex([pd.Timestamp('2015-02-11'),
                   None, pd.Timestamp(''), pd.NaT])

# Print the Datetime Index
idx
```

**输出:**
![](img/a89d26a278de4b85f55465573fb65e55.png)

现在，我们将检查 Datetime 索引中的标签是否存在或缺失。

```py
# test whether the passed Datetime Index
# labels are missing or not.
idx.isnull()
```

**输出:**
![](img/4e95644dfa797f01e4b78600cac85221.png)

正如我们在输出中看到的，该函数返回了一个数组对象，其大小与 Datetime 索引的大小相同。`True`值表示索引标签缺失，`False`值表示索引标签未缺失。
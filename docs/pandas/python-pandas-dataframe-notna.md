# python | pandas data frame . note()

> 原文:[https://www . geesforgeks . org/python-pandas-data frame-notna/](https://www.geeksforgeeks.org/python-pandas-dataframe-notna/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。
熊猫**数据框. notna()** 功能检测数据框中现有的/非缺失的值。该函数返回一个布尔对象，该对象的大小与应用它的对象的大小相同，指示每个单独的值是否为 na 值。所有非缺失值都被映射为 true，缺失值被映射为 false。
**注意:**空字符串”或 numpy.inf 等字符不视为 NA 值。(除非你设置 pandas . options . mode . use _ INF _ as _ na = True)。

> **语法:** DataFrame.notna()
> **返回:**data frame 中每个元素的布尔值掩码，指示某个元素是否不是安娜值

**示例#1:** 使用 notna()函数查找数据帧中所有未缺失的值。

## 蟒蛇 3

```py
# importing pandas as pd
import pandas as pd

# Creating the first dataframe
df = pd.DataFrame({"A":[14, 4, 5, 4, 1],
                   "B":[5, 2, 54, 3, 2],
                   "C":[20, 20, 7, 3, 8],
                   "D":[14, 3, 6, 2, 6]})

# Print the dataframe
df
```

![](img/291aa2ed401398537f5e3626ac2c5b81.png)

让我们使用 dataframe.notna()函数来查找 dataframe 中所有未丢失的值。

## 蟒蛇 3

```py
# find non-na values
df.notna()
```

**输出:**

![](img/2eaa26563f67c74e3b59126432e542b5.png)

正如我们在输出中看到的，dataframe 中所有未丢失的值都被映射为 true。没有错误值，因为数据帧中没有缺失值。

**示例#2:** 当数据帧中有缺失值时，使用 notna()函数查找非缺失值。

## 蟒蛇 3

```py
# importing pandas as pd
import pandas as pd

# Creating the dataframe
df = pd.DataFrame({"A":[12, 4, 5, None, 1],
                   "B":[7, 2, 54, 3, None],
                   "C":[20, 16, 11, 3, 8],
                   "D":[14, 3, None, 2, 6]})

# find non-missing values
df.notna()
```

**输出:**

![](img/d9d852d6ab9c2efaaa25b412ce7718a2.png)

正如我们在输出中看到的，具有 na 值的单元格被映射为假，所有具有非缺失值的单元格被映射为真。
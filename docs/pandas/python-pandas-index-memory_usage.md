# Python | Pandas index . memory _ usage()

> 原文:[https://www . geesforgeks . org/python-pandas-index-memory _ usage/](https://www.geeksforgeeks.org/python-pandas-index-memory_usage/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

熊猫 **Index.memory_usage()** 函数返回索引的内存使用情况。它返回索引中所有单个标签使用的内存总和

> **语法:**index . memory _ usage(deep = False)
> **参数:**
> **deep :** 深入检查数据，针对系统级内存消耗询问对象数据类型
> **返回:**使用的字节数

**示例#1:** 使用 Index.memory_usage()函数查找 Index 对象使用的总内存。

## 蟒蛇 3

```
# importing pandas as pd
import pandas as pd

# Creating the Index
idx = pd.Index(['Labrador', 'Beagle', 'Mastiff', 'Lhasa', 'Husky', 'Beagle'])

# Print the Index
idx
```

**输出:**

![](img/49501e3b227ab712536e6e913bfad999.png)

现在我们将使用 Index.memory_usage()函数来查找 idx 对象的内存使用情况。

## 蟒蛇 3

```
# finding the memory used by the idx object
idx.memory_usage()
```

**输出:**

![](img/e0f4d67b63990dbe697d210d4298bddd.png)

该函数返回的值为 48，表示正在使用 48 字节的内存。

**示例 2:** 使用 Index.memory_usage()函数检查 MultiIndex 对象的内存使用情况。

## 蟒蛇 3

```
# importing pandas as pd
import pandas as pd

# Creating the MultiIndex
midx = pd.MultiIndex.from_arrays([['Mon', 'Tue', 'Wed', 'Thr'], [10, 20, 30, 40]],
                                                       names =('Days', 'Target'))

# Print the MultiIndex
midx
```

**输出:**

![](img/8700240de382239efa5756f7e592fea0.png)

现在我们将检查 midx 对象使用的内存量。

## 蟒蛇 3

```
# return the total memory used by the multi-index object
midx.memory_usage()
```

**输出:**

![](img/5f252918a3ec4035c0c4cc40b4810399.png)

正如我们在输出中看到的，函数返回了 180，表明 midx 对象正在使用 180 字节的内存。
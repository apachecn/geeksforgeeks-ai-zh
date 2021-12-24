# Python | Pandas data frame . tz _ convert

> 原文:[https://www . geesforgeks . org/python-pandas-data frame-tz _ convert/](https://www.geeksforgeeks.org/python-pandas-dataframe-tz_convert/)

Pandas DataFrame 是一个二维可变大小、潜在异构的表格数据结构，带有标记轴(行和列)。算术运算在行标签和列标签上对齐。它可以被认为是系列对象的类似字典的容器。这是熊猫的主要数据结构。

熊猫 `**DataFrame.tz_convert()**`功能用于将 tz 感知轴转换为目标时区。

> **语法:** DataFrame.tz_convert(tz，轴=0，级别=无，复制=真)
> 
> **参数:**
> **tz :** 字符串或 pytz.timezone 对象
> **轴:**要转换的轴
> **级别:**如果轴是一个 MultiIndex，则转换一个特定级别。否则必须为无
> **副本:**同时复制底层数据
> 
> **返回:** tz 转换后的数据帧

**示例#1:** 使用`DataFrame.tz_convert()`函数转换给定数据框的时区。

```py
# importing pandas as pd
import pandas as pd

# Creating the DataFrame
df = pd.DataFrame({'Weight':[45, 88, 56, 15, 71],
                   'Name':['Sam', 'Andrea', 'Alex', 'Robin', 'Kia'],
                   'Age':[14, 25, 55, 8, 21]})

# Create the index
index_ = pd.date_range('2010-10-09 08:45', periods = 5, freq ='H', tz = 'US / Central')

# Set the index
df.index = index_

# Print the DataFrame
print(df)
```

**输出:**
![](img/a98bc6dd87f7561204138ad3e9e5cf1d.png)

现在我们将使用`DataFrame.tz_convert()`功能将给定数据帧的时区转换为“欧洲/柏林”。

```py
# Let's find out the current timezone
# of the given dataframe
print(df.index)

# Let's convert the timezone of the
# dataframe to 'Europe / Berlin'
df = df.tz_convert(tz = 'Europe / Berlin')

# Let's find out the current timezone
# of the given dataframe
print(df.index) 
```

**输出:**
![](img/80e5e15423b570da31638ee0a256661c.png)
![](img/475299228cca99e6b32fcd501a50d55c.png)

正如我们在输出中看到的那样，`DataFrame.tz_convert()`函数已经成功地将给定数据帧的时区转换为所需的时区。

**示例 2 :** 使用`DataFrame.tz_convert()`函数转换给定数据帧的时区。给定数据帧的索引是多索引。

```py
# importing pandas as pd
import pandas as pd

# Creating the DataFrame
df = pd.DataFrame({'Weight':[45, 88, 56, 15, 71],
                   'Name':['Sam', 'Andrea', 'Alex', 'Robin', 'Kia'],
                   'Age':[14, 25, 55, 8, 21]})

# Create the MultiIndex
index_ = pd.MultiIndex.from_product([['Date'], pd.date_range('2010-10-09 08:45', periods = 5, freq ='H', tz = 
             'US/Central')], names =['Level 1', 'Level 2'])

# Set the index
df.index = index_

# Print the DataFrame
print(df)
```

**输出:**

![](img/2ab39eee57eacdfac3dbf339d78326ec.png)

现在，我们将使用`DataFrame.tz_convert()`函数将给定数据帧中多索引级别 1 的时区转换为“欧洲/柏林”。

```py
# Let's find out the current timezone
# of the Level 1 of the given dataframe
print(df.index[1])

# Let's convert the timezone of the
# level 1 of the dataframe to 'Europe / Berlin'
df = df.tz_convert(tz = 'Europe/Berlin', level = 1)

# Let's find out the current timezone
# of the level 1 of the given dataframe
print(df.index[1]) 
```

**输出:**

![](img/b25c820505b575d0954495ae7342327b.png)

![](img/7be84c707eaae2835154b69dbfe58244.png)

正如我们在输出中看到的那样，`DataFrame.tz_convert()`函数已经成功地将给定数据帧中所需级别的时区转换为所需时区。
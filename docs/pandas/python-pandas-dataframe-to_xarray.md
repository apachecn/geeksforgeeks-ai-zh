# Python | Pandas data frame . to _ xarray

> 原文:[https://www . geesforgeks . org/python-pandas-data frame-to _ xarray/](https://www.geeksforgeeks.org/python-pandas-dataframe-to_xarray/)

Pandas DataFrame 是一个二维可变大小、潜在异构的表格数据结构，带有标记轴(行和列)。算术运算在行标签和列标签上对齐。它可以被认为是系列对象的类似字典的容器。这是熊猫的主要数据结构。

熊猫 `**DataFrame.to_xarray()**`函数从熊猫对象返回一个 xarray 对象。

> **语法:** DataFrame.to_xarray()
> 
> **参数:**无
> 
> **返回:** xarray。DataArray 或 xarray。资料组

**示例#1:** 使用`DataFrame.to_xarray()`函数使用给定的数据帧构建一个 xarray 对象。

```py
# importing pandas as pd
import pandas as pd

# Creating the DataFrame
df = pd.DataFrame({'Weight':[45, 88, 56, 15, 71],
                   'Name':['Sam', 'Andrea', 'Alex', 'Robin', 'Kia'],
                   'Age':[14, 25, 55, 8, 21]})

# Create the index
index_ = pd.date_range('2010-10-09 08:45', periods = 5, freq ='H')

# Set the index
df.index = index_

# Print the DataFrame
print(df)
```

**输出:**
![](img/a98bc6dd87f7561204138ad3e9e5cf1d.png)

现在，我们将使用`DataFrame.to_xarray()`函数，使用给定的数据帧构建一个 xarray 对象。

```py
# return an xarray object
result = df.to_xarray()

# Print the result
print(result)
```

**输出:**
![](img/7cfa1594425678cf59acdf1858193120.png)

正如我们在输出中看到的那样，`DataFrame.to_xarray()`函数已经成功地使用给定的数据帧构建了一个 xarray 对象。

**示例 2:** 使用`DataFrame.to_xarray()`函数使用给定的数据帧构建一个 xarray 对象。

```py
# importing pandas as pd
import pandas as pd

# Creating the DataFrame
df = pd.DataFrame({"A":[12, 4, 5, None, 1], 
                   "B":[7, 2, 54, 3, None], 
                   "C":[20, 16, 11, 3, 8], 
                   "D":[14, 3, None, 2, 6]}) 

# Create the index
index_ = ['Row_1', 'Row_2', 'Row_3', 'Row_4', 'Row_5']

# Set the index
df.index = index_

# Print the DataFrame
print(df)
```

**输出:**
![](img/0b8a01d9a4a8d2a41f2d5f3dbdf72d6b.png)

现在，我们将使用`DataFrame.to_xarray()`函数，使用给定的数据帧构建一个 xarray 对象。

```py
# return an xarray object
result = df.to_xarray()

# Print the result
print(result)
```

**输出:**
![](img/2164bda4f7e9579cbb3c642ad0998773.png)
正如我们在输出中看到的，`DataFrame.to_xarray()`函数已经成功地使用给定的数据帧构建了一个 xarray 对象。
# Python | Pandas data frame . to _ sparse

> 原文:[https://www . geesforgeks . org/python-pandas-data frame-to _ sparse/](https://www.geeksforgeeks.org/python-pandas-dataframe-to_sparse/)

Pandas DataFrame 是一个二维可变大小、潜在异构的表格数据结构，带有标记轴(行和列)。算术运算在行标签和列标签上对齐。它可以被认为是系列对象的类似字典的容器。这是熊猫的主要数据结构。

熊猫 `**DataFrame.to_sparse()**`功能转换为稀疏帧。该函数实现了数据帧的稀疏版本，这意味着任何与特定值匹配的数据都会在表示中被省略。稀疏数据帧允许更高效的存储。

> **语法:**data frame . to _ sparse(fill _ value = None，kind='block ')
> 
> **参数:**
> **fill_value :** 表示法中应省略的具体值。
> **种类:** {'block '，' integer'}，默认为' block '
> 
> **返回:**稀疏参数

**示例#1:** 使用`DataFrame.to_sparse()`函数将给定的数据帧转换为稀疏数据帧，以实现高效存储。

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

现在我们将使用`DataFrame.to_sparse()`函数将给定的数据帧转换为稀疏数据帧。

```py
# convert to SparseDataFrame
result = df.to_sparse()

# Print the result
print(result)

# Verify the result by checking the 
# type of the object.
print(type(result))
```

**输出:**
![](img/a98bc6dd87f7561204138ad3e9e5cf1d.png)
![](img/9fcaee3bee25fcfca24bd172da214f3a.png)

正如我们在输出中看到的那样，`DataFrame.to_sparse()`函数已经成功地将给定的数据帧转换为稀疏数据帧类型。

**示例 2:** 使用`DataFrame.to_sparse()`函数将给定的数据帧转换为稀疏数据帧，以实现高效存储。

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

现在我们将使用`DataFrame.to_sparse()`函数将给定的数据帧转换为稀疏数据帧。

```py
# convert to SparseDataFrame
result = df.to_sparse()

# Print the result
print(result)

# Verify the result by checking the 
# type of the object.
print(type(result))
```

**输出:**
![](img/0b8a01d9a4a8d2a41f2d5f3dbdf72d6b.png)
![](img/9fcaee3bee25fcfca24bd172da214f3a.png)
正如我们在输出中看到的，`DataFrame.to_sparse()`函数已经成功地将给定的数据帧转换为稀疏数据帧类型。
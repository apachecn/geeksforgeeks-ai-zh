# Python | Pandas data frame . columns

> 原文:[https://www . geesforgeks . org/python-pandas-data frame-columns/](https://www.geeksforgeeks.org/python-pandas-dataframe-columns/)

Pandas DataFrame 是一个二维可变大小、潜在异构的表格数据结构，带有标记轴(行和列)。算术运算在行标签和列标签上对齐。它可以被认为是系列对象的类似字典的容器。这是熊猫的主要数据结构。

熊猫 `**DataFrame.columns**`属性返回给定数据帧的列标签。

> **语法:**数据帧.列
> 
> **参数:**无
> 
> **返回:**列名

**示例#1:** 使用`DataFrame.columns`属性返回给定数据框的列标签。

```py
# importing pandas as pd
import pandas as pd

# Creating the DataFrame
df = pd.DataFrame({'Weight':[45, 88, 56, 15, 71],
                   'Name':['Sam', 'Andrea', 'Alex', 'Robin', 'Kia'],
                   'Age':[14, 25, 55, 8, 21]})

# Create the index
index_ = ['Row_1', 'Row_2', 'Row_3', 'Row_4', 'Row_5']

# Set the index
df.index = index_

# Print the DataFrame
print(df)
```

**输出:**
![](img/64424eb76121875ed8cceabce6670c8d.png)

现在我们将使用`DataFrame.columns`属性返回给定数据帧的列标签。

```py
# return the column labels
result = df.columns

# Print the result
print(result)
```

**输出:**
![](img/d2dd237e06d7768f77ab2524f9b21492.png)
正如我们在输出中看到的，`DataFrame.columns`属性已经成功返回了给定数据帧的所有列标签。

**示例 2:** 使用`DataFrame.columns`属性返回给定数据框的列标签。

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

![](img/e50745467d928264bfba5bfaec717bdc.png)

现在我们将使用`DataFrame.columns`属性返回给定数据帧的列标签。

```py
# return the column labels
result = df.columns

# Print the result
print(result)
```

**输出:**
![](img/268c1f2258d8ae97b5189290157cef25.png)
正如我们在输出中看到的，`DataFrame.columns`属性已经成功返回了给定数据帧的所有列标签。
# python | pandas data frame . loc[]

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python 熊猫 dataframe-loc/

Pandas DataFrame 是一个二维可变大小、潜在异构的表格数据结构，带有标记轴(行和列)。算术运算在行标签和列标签上对齐。它可以被认为是系列对象的类似字典的容器。这是熊猫的主要数据结构。

熊猫 `**DataFrame.loc**`属性通过给定数据帧中的标签或布尔数组访问一组行和列。

> **语法:** DataFrame.loc
> 
> **参数:**无
> 
> **返回:**标量、序列、数据帧

**示例#1:** 使用`DataFrame.loc`属性使用索引和列标签访问给定数据框中的特定单元格。

```
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

现在，我们将使用`DataFrame.loc`属性返回“行 _2”标签对应的“名称”列中的值。

```
# return the value
result = df.loc['Row_2', 'Name']

# Print the result
print(result)
```

**输出:**
![](img/07a1d05c8b4ee6a61ecf7061cbcae77e.png)
正如我们在输出中看到的那样，`DataFrame.loc`属性已经成功地返回了给定数据帧中所需位置的值。

**示例 2:** 使用`DataFrame.loc`属性返回给定数据框中的两列。

```
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

现在我们将使用`DataFrame.loc`属性返回数据框的“A”和“D”列中的值。

```
# return the values.
result = df.loc[:, ['A', 'D']]

# Print the result
print(result)
```

**输出:**
![](img/1aa66e4712ad56d6158f2cb4494c24b9.png)
正如我们在输出中看到的，`DataFrame.loc`属性已经成功地返回了数据框的所需列。
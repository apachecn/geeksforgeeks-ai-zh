# python | pandas data frame . dtype

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python 熊猫 data frame-dttypes/

Pandas DataFrame 是一个二维可变大小、潜在异构的表格数据结构，带有标记轴(行和列)。算术运算在行标签和列标签上对齐。它可以被认为是系列对象的类似字典的容器。这是熊猫的主要数据结构。

熊猫 `**DataFrame.dtypes**`属性返回数据框中的数据类型。它返回一个包含每列数据类型的序列。

> **语法:**数据帧.数据类型
> 
> **参数:**无
> 
> **返回:**每列的数据类型

**示例#1:** 使用`DataFrame.dtypes`属性找出给定数据框中每列的数据类型(数据类型)。

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
现在我们使用`DataFrame.dtypes`属性找出给定数据帧中每一列的数据类型。

```
# return the dtype of each column
result = df.dtypes

# Print the result
print(result)
```

**输出:**
![](img/70fcd54459db07c7bfdac93bd08cabc9.png)
正如我们在输出中看到的，`DataFrame.dtypes`属性已经成功地返回了给定数据框中每一列的数据类型。

**例 2:** 使用`DataFrame.dtypes`属性找出给定数据帧中每一列的数据类型(dtype)。

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

现在我们将使用`DataFrame.dtypes`属性找出给定数据帧中每一列的数据类型。

```
# return the dtype of each column
result = df.dtypes

# Print the result
print(result)
```

**输出:**
![](img/81de60830e57d0a49608443fc3869073.png)
正如我们在输出中看到的，`DataFrame.dtypes`属性已经成功返回了给定数据框中每一列的数据类型。
# python | pandas data frame . axes

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python 熊猫 dataframe-axes/

Pandas DataFrame 是一个二维可变大小、潜在异构的表格数据结构，带有标记轴(行和列)。算术运算在行标签和列标签上对齐。它可以被认为是系列对象的类似字典的容器。这是熊猫的主要数据结构。

熊猫 `**DataFrame.axes**`属性通过给定数据帧中的标签或布尔数组访问一组行和列。

> **语法:**数据框轴
> 
> **参数:**无
> 
> **返回:**列表

**示例#1:** 使用`DataFrame.axes`属性返回包含数据框轴标签的列表。

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

现在我们将使用`DataFrame.axes`属性返回数据框的轴标签。

```py
# return the axes labels of the dataframe
result = df.axes

# Print the result
print(result)
```

**输出:**
![](img/aed0910373503f74ab86a8dc80b1f2a7.png)
正如我们在输出中看到的，`DataFrame.axes`属性已经成功返回了包含数据框轴标签的列表。

**示例 2:** 使用`DataFrame.axes`属性返回包含数据框轴标签的列表。

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

现在我们将使用`DataFrame.axes`属性返回数据框的轴标签。

```py
# return the axes labels of the dataframe
result = df.axes

# Print the result
print(result)
```

**输出:**
![](img/7a503f2dca1e8572635b1cf528ecf398.png)
正如我们在输出中看到的，`DataFrame.axes`属性已经成功返回了一个包含数据框坐标轴标签的列表。
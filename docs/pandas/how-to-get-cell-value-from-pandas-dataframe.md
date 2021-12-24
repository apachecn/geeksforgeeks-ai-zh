# 如何从熊猫数据框中获取细胞值？

> 原文:[https://www . geeksforgeeks . org/如何从熊猫获取细胞价值-dataframe/](https://www.geeksforgeeks.org/how-to-get-cell-value-from-pandas-dataframe/)

在本文中，我们将讨论如何从熊猫数据框中获取细胞值。

## 方法一:使用 [loc()](https://www.geeksforgeeks.org/python-pandas-dataframe-loc/) 功能

此方法用于通过使用列名获取具有索引功能的特定单元格数据

**语法**:

> dataframe['column_name']。loc[data frame . index[row _ number]]

哪里，

*   数据帧是输入数据帧
*   index 是获取单元格的 row _ numer 的函数
*   column_name 表示单元格的列名

**示例**:使用 loc()函数获取特定单元格的 Python 程序

## 蟒蛇 3

```py
# import pandas module
import pandas as pd

# create dataframe with 3 columns
data = pd.DataFrame({
    "id": [7058, 7059, 7072, 7054],
    "name": ['sravan', 'jyothika', 'harsha', 'ramya'],
    "subjects": ['java', 'python', 'html/php', 'php/js']
}
)

# get the cell value using loc() function
# in id column and 1 row
print(data['id'].loc[data.index[0]])

# get the cell value using loc() function
# in id column and 2 row
print(data['id'].loc[data.index[1]])

# get the cell value using loc() function
# in id column and 3 row
print(data['id'].loc[data.index[2]])

# get the cell value using loc() function
# in id column and 4 row
print(data['id'].loc[data.index[3]])

# get the cell value using loc() function
# in name column and 1 row
print(data['name'].loc[data.index[0]])

# get the cell value using loc() function
# in name column and 2 row
print(data['name'].loc[data.index[1]])

# get the cell value using loc() function
# in subjects column and 3 row
print(data['subjects'].loc[data.index[2]])

# get the cell value using loc() function
# in subjects column and 4 row
print(data['subjects'].loc[data.index[3]])
```

**输出:**

```py
7058
7059
7072
7054
sravan
jyothika
html/php
php/js
```

## 方法二:使用[iloc【】](https://www.geeksforgeeks.org/python-extracting-rows-using-pandas-iloc/)

此方法用于通过使用列名和行索引号来访问单元格数据。

**语法**:

> dataframe['column_name']。iloc[行号]

在哪里

*   数据帧是输入数据帧
*   row _ numer 表示单元格的单元格行位置
*   column_name 表示单元格的列名

**示例**:使用 iloc 函数获取单元格值的 Python 程序

## 蟒蛇 3

```py
# import pandas module
import pandas as pd

# create dataframe with 3 columns
data = pd.DataFrame({
    "id": [7058, 7059, 7072, 7054],
    "name": ['sravan', 'jyothika', 'harsha', 'ramya'],
    "subjects": ['java', 'python', 'html/php', 'php/js']
}
)

# get the cell value using iloc() function
# in id column and 1 row
print(data['id'].iloc[0])

# get the cell value using iloc() function
# in id column and 2 row
print(data['id'].iloc[1])

# get the cell value using iloc() function
# in name column and 1 row
print(data['name'].iloc[0])

# get the cell value using iloc() function
# in id column and 4 row
print(data['name'].iloc[3])

# get the cell value using iloc() function
# in subjects column and 1 row
print(data['subjects'].iloc[0])

# get the cell value using iloc() function
# in subjects column and 4 row
print(data['subjects'].iloc[3])
```

**输出:**

```py
7058
7059
sravan
ramya
java
php/js
```

## 方法 3:使用 values()函数

这将通过提供行号和列名来返回单元格值。

**语法**:

> dataframe['column_name']。值[行号]

哪里，

*   数据帧是输入数据帧
*   row _ numer 表示单元格的单元格行位置
*   column_name 表示单元格的列名

**示例:**从数据框中获取单元格值的 Python 代码

## 蟒蛇 3

```py
# import pandas module
import pandas as pd

# create dataframe with 3 columns
data = pd.DataFrame({
    "id": [7058, 7059, 7072, 7054],
    "name": ['sravan', 'jyothika', 'harsha', 'ramya'],
    "subjects": ['java', 'python', 'html/php', 'php/js']
}
)

# get the cell value using values() function
# in id column and 1 row
print(data['name'].values[0])

# get the cell value using values() function
# in id column and 2 row
print(data['id'].values[1])

# get the cell value using values() function
# in name column and 1 row
print(data['name'].values[0])

# get the cell value using values() function
# in id column and 4 row
print(data['name'].values[3])

# get the cell value using values() function
# in subjects column and 1 row
print(data['subjects'].values[0])

# get the cell value using values() function
# in subjects column and 4 row
print(data['subjects'].values[3])
```
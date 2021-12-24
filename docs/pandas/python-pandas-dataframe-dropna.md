# python | pandas data frame . drop na()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python 熊猫 dataframe-dropna/

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 python 包的奇妙生态系统。Pandas 就是其中之一，它让数据的导入和分析变得更加容易。

有时 csv 文件有空值，这些值后来在数据框中显示为 NaN。Pandas *dropna()* 方法允许用户以不同的方式分析和删除空值的行/列。

**语法:**

```
DataFrameName.dropna(axis=0, how='any', thresh=None, subset=None, inplace=False)
```

**参数:**

> **轴:**轴取行/列的 int 或 string 值。整数的输入可以是 0 或 1，字符串的输入可以是“索引”或“列”。
> **how:** how 只取两种字符串值(‘any’或‘all’)。如果 any 值为空，则“ANY”删除行/列，如果 all 值为空，则“ALL”删除行/列。
> **thresh:** thresh 取整数值，表示 na 值下降的最小值。
> **子集:**它是一个数组，将删除过程限制在通过列表传递的行/列。
> **inplace:** 是一个布尔值，如果为 True，则改变数据框本身。

有关代码中使用的 CSV 文件的链接，请单击此处的[。](https://drive.google.com/open?id=1Uzdua5o61cfXMz1K16NNcwLFqG91J6W4)

**示例#1:** 删除至少有 1 个空值的行。

读取数据框，并删除所有具有空值的行。比较新旧数据框的大小，看看有多少行至少有 1 个空值。

```
# importing pandas module
import pandas as pd

# making data frame from csv file
data = pd.read_csv("nba.csv")

# making new data frame with dropped NA values
new_data = data.dropna(axis = 0, how ='any')

# comparing sizes of data frames
print("Old data frame length:", len(data), "\nNew data frame length:", 
       len(new_data), "\nNumber of rows with at least 1 NA value: ",
       (len(data)-len(new_data)))
```

**输出:**

```
Old data frame length:  458 
New data frame length:  364 
Number of rows with at least 1 NA value:  94

```

因为差异是 94，所以有 94 行在任何列中都至少有 1 个空值。

**示例#2:** 更改轴并使用方式和位置参数

制作了两个数据帧。所有值都=无的列将被添加到新的数据框中。验证列名以查看是否正确插入了空列。然后比较删除 NaN 值前后的列数。

```
# importing pandas module
import pandas as pd

# making data frame from csv file
data = pd.read_csv("nba.csv")

# making a copy of old data frame
new = pd.read_csv("nba.csv")

# creating a value with all null values in new data frame
new["Null Column"]= None

# checking if column is inserted properly 
print(data.columns.values, "\n", new.columns.values)

# comparing values before dropping null column
print("\nColumn number before dropping Null column\n",
       len(data.dtypes), len(new.dtypes))

# dropping column with all null values
new.dropna(axis = 1, how ='all', inplace = True)

# comparing values after dropping null column
print("\nColumn number after dropping Null column\n",
      len(data.dtypes), len(new.dtypes))
```

**输出:**

```
['Name' 'Team' 'Number' 'Position' 'Age' 'Height' 'Weight' 'College'
 'Salary'] 
 ['Name' 'Team' 'Number' 'Position' 'Age' 'Height' 'Weight' 'College'
 'Salary' 'Null Column']

Column number before dropping Null column
 9 10

Column number after dropping Null column
 9 9

```
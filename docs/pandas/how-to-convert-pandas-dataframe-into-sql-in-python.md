# 如何用 Python 将熊猫 DataFrame 转换成 SQL？

> 原文:[https://www . geeksforgeeks . org/如何将 pandas-dataframe 转换为 python 中的 SQL/](https://www.geeksforgeeks.org/how-to-convert-pandas-dataframe-into-sql-in-python/)

在本文中，我们旨在将数据框转换为 SQL 数据库，然后尝试使用 SQL 查询或通过表从 SQL 数据库中读取内容

为了用 python 处理 SQL，我们需要通过在 cmd 中运行下面提到的命令来安装 sqlalchemy 库:

```
 pip install sqlalchemy 
```

有必要创建一个熊猫数据框架，以进一步进行。

## 蟒蛇 3

```
# import pandas library
import pandas as pd

# create a dataframe
# object from dictionary
dataset = pd.DataFrame({'Names':['Abhinav','Aryan',
                                 'Manthan'],
                        'DOB' : ['10/01/2009','24/03/2009',
                                '28/02/2009']})
# show the dataframe
print(dataset)
```

**输出:**

```
     Names         DOB
0  Abhinav  10/01/2009
1    Aryan  24/03/2009
2  Manthan  28/02/2009
```

创建数据集后，我们需要将数据框连接到为 sqlite3 提供的数据库支持。连接对象。

## 蟒蛇 3

```
#importing sql library
from sqlalchemy import create_engine

# create a reference
# for sql library
engine = create_engine('sqlite://',
                       echo = False)

# attach the data frame to the sql
# with a name of the table
# as "Employee_Data"
dataset.to_sql('Employee_Data',
               con = engine)

# show the complete data
# from Employee_Data table
print(engine.execute("SELECT * FROM Employee_Data").fetchall())
```

**输出:**

```
[(0, 'Abhinav', '10/01/2009'), (1, 'Aryan', '24/03/2009'), 
(2, 'Manthan', '28/02/2009')]
```

将数据添加到数据库后，它以记录的形式对我们可见。数据也可以附加到先前创建的数据库，如下所示:

## 蟒蛇 3

```
# Create a dataframe
# object from dictionary
df1 = pd.DataFrame({'Names' : ['Sonia', 'Priya'],
                    'DOB':['18/10/2009','14/06/2009']})

# appending new data frame
# to existing data frame
df1.to_sql('Employee_Data',
           con = engine,
           if_exists = 'append')

# run a sql query
print(engine.execute("SELECT * FROM Employee_Data").fetchall())
```

**输出:**

```
[(0, 'Abhinav', '10/01/2009'), (1, 'Aryan', '24/03/2009'),
 (2, 'Manthan', '28/02/2009'), (0, 'Sonia', '18/10/2009'),
  (1, 'Priya', '14/06/2009')]
```

从上面的例子可以理解，虽然添加了数据，但是只有当添加了新的数据帧时，索引才从 0 开始。数据框可以被传输到 SQL 数据库，同样的数据框也可以从 SQL 数据库中读取。read_sql 的返回类型是数据帧。

## 蟒蛇 3

```
# reading the sql database
# with index "Names"
df2 = pd.read_sql('Employee_Data',
                  con = engine,
                  index_col = 'Names',
                  parse_dates = ['DOB'])
# show the dataframe
print(df2)

# print new line
print()

# show the type of df2
print(type(df2))
```

**输出:**

```
 id        DOB
Names               
Sonia   0 2009-10-18
Priya   1 2009-06-14
```

我们还可以访问数据库中的特定列，而不是整个表。

## 蟒蛇 3

```
# acccesing only a particular
# column from the database
df3 = pd.read_sql('Employee_Data',
                  con = engine,
                  columns = ["Names"])
# show the data
print(df3)
```

**输出:**

```
Names
0  Sonia
1  Priya
```

如果我们希望数据库中的数据以列表的形式存在，这是可能的。

## 蟒蛇 3

```
# get a particular column
# from a database in the
# form of list
df4 = pd.read_sql('Employee_Data',
                  con = engine,
                  index_col = 'Names',
                  columns = ["Names"])
# show the data
print(df4)
```

**输出:**

```
Empty DataFrame
Columns: []
Index: [Sonia, Priya]
```

可以使用 read_sql_query()命令，通过传递适当的 sql 查询和连接对象，用 python 编写 SQL 查询。

**parse _ date:**该参数有助于将我们这边最初作为日期传递的日期转换为真正的日期格式。

## 蟒蛇 3

```
# run a sql query in the database
# and store result in a dataframe
df5 = pd.read_sql_query('Select DOB from Employee_Data',
                        con = engine,
                        parse_dates = ['DOB'])
# show the dataframe
print(df5)
```

**输出:**

```
   DOB
0 2009-10-18
1 2009-06-14
```
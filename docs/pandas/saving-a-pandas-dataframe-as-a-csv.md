# 将熊猫数据框保存为 CSV

> 原文:[https://www . geesforgeks . org/saving-a-pandas-data frame-as-a-CSV/](https://www.geeksforgeeks.org/saving-a-pandas-dataframe-as-a-csv/)

熊猫是一个开源库，建立在 NumPy 库之上。它允许用户快速分析、数据清理和有效地准备数据。Pandas 速度快，对用户来说具有高性能和高生产率。

您使用的大多数数据集都称为数据帧。数据框是一个二维标记的数据结构，带有行和列的索引，其中每个单元格用于存储任何类型的值。基本上，数据帧是基于字典的 NumPy 数组。

让我们看看如何使用`to_csv()`方法将熊猫数据帧保存为 CSV 文件。

**示例#1:** 将 csv 保存到工作目录。

```py
# importing pandas as pd 
import pandas as pd 

# list of name, degree, score
nme = ["aparna", "pankaj", "sudhir", "Geeku"]
deg = ["MBA", "BCA", "M.Tech", "MBA"]
scr = [90, 40, 80, 98]

# dictionary of lists 
dict = {'name': nme, 'degree': deg, 'score': scr} 

df = pd.DataFrame(dict)

# saving the dataframe
df.to_csv('file1.csv')
```

**输出:**
![](img/783c020eb204c25366d491f7890074f6.png)

**例 2:** 保存 CSV 而不保存*表头*和*索引*。

```py
# importing pandas as pd 
import pandas as pd 

# list of name, degree, score
nme = ["aparna", "pankaj", "sudhir", "Geeku"]
deg = ["MBA", "BCA", "M.Tech", "MBA"]
scr = [90, 40, 80, 98]

# dictionary of lists 
dict = {'name': nme, 'degree': deg, 'score': scr} 

df = pd.DataFrame(dict)

# saving the dataframe
df.to_csv('file2.csv', header=False, index=False)
```

**输出:**
![](img/a02c8b7f379e301de6291a450cb642fa.png)

**示例#3:** 将 csv 文件保存到指定位置。

```py
# importing pandas as pd 
import pandas as pd 

# list of name, degree, score
nme = ["aparna", "pankaj", "sudhir", "Geeku"]
deg = ["MBA", "BCA", "M.Tech", "MBA"]
scr = [90, 40, 80, 98]

# dictionary of lists 
dict = {'name': nme, 'degree': deg, 'score': scr} 

df = pd.DataFrame(dict)

# saving the dataframe
df.to_csv(r'C:\Users\Admin\Desktop\file3.csv', index=False)
```

**输出:**
![](img/1078d3208bebb7823362d3764243a86f.png)

**示例#4:** 使用制表符分隔符将数据帧写入 CSV 文件。

```py
import pandas as pd
import numpy as np
users = {'Name': ['Amit', 'Cody', 'Drew'],
     'Age': [20,21,25]}
df = pd.DataFrame(users, columns=['Name','Age'])#create DataFrame
print("Original DataFrame:")
print(df)
print('Data from Users.csv:')
df.to_csv('Users.csv', sep='\t', index=False,header=True)
new_df = pd.read_csv('Users.csv')
print(new_df)
```

**输出:**

```py
Original DataFrame:
   Name  Age
0  Amit   20
1  Cody   21
2  Drew   25
Data from Users.csv:
  Name\tAge
0  Amit\t20
1  Cody\t21
2  Drew\t25

```
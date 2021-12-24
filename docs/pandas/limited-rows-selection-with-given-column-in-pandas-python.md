# 熊猫| Python 中给定列的有限行选择

> 原文:[https://www . geesforgeks . org/limited-row-selection-with-given-in-pandas-python/](https://www.geeksforgeeks.org/limited-rows-selection-with-given-column-in-pandas-python/)

熊猫中的方法如`iloc[]`、`iat[]` 一般用于从给定的数据帧中选择数据。在本文中，我们将学习如何在这些方法的帮助下选择给定列的有限行。

**示例 1:** 选择两列

```
# Import pandas package 
import pandas as pd 

# Define a dictionary containing employee data 
data = {'Name':['Jai', 'Princi', 'Gaurav', 'Anuj'], 
        'Age':[27, 24, 22, 32], 
        'Address':['Delhi', 'Kanpur', 'Allahabad', 'Kannauj'], 
        'Qualification':['Msc', 'MA', 'MCA', 'Phd']} 

# Convert the dictionary into DataFrame  
df = pd.DataFrame(data) 

# select three rows and two columns 
print(df.loc[1:3, ['Name', 'Qualification']])
```

**输出:**

```
     Name Qualification
1  Princi            MA
2  Gaurav           MCA
3    Anuj           Phd

```

**示例 2:** 首先按标签格式过滤行和选择列，然后选择所有列。

```
# Import pandas package 
import pandas as pd 

# Define a dictionary containing employee data 
data = {'Name':['Jai', 'Princi', 'Gaurav', 'Anuj'], 
        'Age':[27, 24, 22, 32], 
        'Address':['Delhi', 'Kanpur', 'Allahabad', 'Kannauj'], 
        'Qualification':['Msc', 'MA', 'MCA', 'Phd'] 
       } 

# Convert the dictionary into DataFrame  
df = pd.DataFrame(data) 

# .loc DataFrame method 
# filtering rows and selecting columns by label format 
# df.loc[rows, columns] 
# row 1, all columns 
print(df.loc[0, :] )
```

**输出:**

```
Address          Delhi
Age                 27
Name               Jai
Qualification      Msc
Name: 0, dtype: object

```

**示例 3:** 选择所有或部分列，使用 iloc 逐个选择。

```
# Import pandas package 
import pandas as pd 

# Define a dictionary containing employee data 
data = {'Name':['Jai', 'Princi', 'Gaurav', 'Anuj'], 
        'Age':[27, 24, 22, 32], 
        'Address':['Delhi', 'Kanpur', 'Allahabad', 'Kannauj'], 
        'Qualification':['Msc', 'MA', 'MCA', 'Phd']} 

# Convert the dictionary into DataFrame  
df = pd.DataFrame(data) 

# iloc[row slicing, column slicing] 
print(df.iloc [0:2, 1:3] )
```

**输出:**

```
   Age    Name
0   27     Jai
1   24  Princi

```
# Python 程序在熊猫中执行交叉连接

> 原文:[https://www . geesforgeks . org/python-程序执行-交叉加入-pandas/](https://www.geeksforgeeks.org/python-program-to-perform-cross-join-in-pandas/)

在熊猫中，[有参数在两个数据帧或系列上执行左、右、内或外合并和连接](https://www.geeksforgeeks.org/python-pandas-merging-joining-and-concatenating/)。然而，目前还不可能使用`how="cross"`参数执行交叉连接来合并或连接两个方法。

**交叉连接:**
![](img/8cf056bbb57d8f3bb2d51c1af3f5690d.png)
![](img/3d754c6f3b663632bf20ae0891213a34.png)

**例 1:**

上面的例子证明如下

```
# importing pandas module
import pandas as pd 

# Define a dictionary with column A
data1 = {'A': [1, 2]} 

# Define another dictionary with column B
data2 = {'B': ['a', 'b', 'c']}  

# Convert the dictionary into DataFrame  
df = pd.DataFrame(data1, index =[0, 1])

# Convert the dictionary into DataFrame  
df1 = pd.DataFrame(data2, index =[2, 3, 4]) 

# Now to perform cross join, we will create
# a key column in both the DataFrames to 
# merge on that key.
df['key'] = 1
df1['key'] = 1

# to obtain the cross join we will merge 
# on the key and drop it.
result = pd.merge(df, df1, on ='key').drop("key", 1)

result
```

**数据帧 1:** ![](img/1da8eef096d67c709cfba88f66ca2a08.png)
**数据帧 2 :** ![](img/f8762271ffb4c64600257b15684bbdd0.png)
**输出:** ![](img/b075fae2f59e8034d77554e0061cc3fc.png)

**例 2:**

用户和产品的两个数据框交叉连接。

```
# importing pandas module
import pandas as pd 

# Define a dictionary containing user ID
data1 = {'Name': ["Rebecca", "Maryam", "Anita"],
        'UserID': [1, 2, 3]} 

# Define a dictionary containing product ID 
data2 = {'ProductID': ['P1', 'P2', 'P3', 'P4']} 

# Convert the dictionary into DataFrame  
df = pd.DataFrame(data1, index =[0, 1, 2])

# Convert the dictionary into DataFrame  
df1 = pd.DataFrame(data2, index =[2, 3, 6, 7]) 

# Now to perform cross join, we will create
# a key column in both the DataFrames to 
# merge on that key.
df['key'] = 1
df1['key'] = 1

# to obtain the cross join we will merge on 
# the key and drop it.
result = pd.merge(df, df1, on ='key').drop("key", 1)

result
```

**数据帧 1:** ![](img/adbab4274c27306e0fe8444bf6a41347.png)
**数据帧 2 :** ![](img/9378f216a89049351fafcc4fd5e35f1f.png)
**输出:** ![](img/6a056cca8cc7f8f3a2b4c55ce482b9b5.png)

**例 3:**

```
# importing pandas module
import pandas as pd 

# Define a dictionary with two columns
data1 = {'col 1': [0, 1],
        'col 2': [2, 3]} 

# Define another dictionary 
data2 = {'col 3': [5, 6],
        'col 4': [7, 8]}  

# Convert the dictionary into DataFrame  
df = pd.DataFrame(data1, index =[0, 1])

# Convert the dictionary into DataFrame  
df1 = pd.DataFrame(data2, index =[2, 3]) 

# Now to perform cross join, we will create
# a key column in both the DataFrames to
# merge on that key.
df['key'] = 1
df1['key'] = 1

# to obtain the cross join we will merge on 
# the key and drop it.
result = pd.merge(df, df1, on ='key').drop("key", 1)

result
```

**数据帧 1:** ![](img/523b4b239a22ea15d360ea61eab14566.png)
**数据帧 2 :** ![](img/a387a5399012114769a0d3d22e5114d6.png)
**输出:** ![](img/6cf4ef427a5cad861aef2ea5446a9c27.png)
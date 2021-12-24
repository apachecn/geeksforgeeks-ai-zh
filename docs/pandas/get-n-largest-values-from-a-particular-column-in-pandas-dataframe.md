# 从熊猫数据框的特定列中获取 n 个最大值

> 原文:[https://www . geesforgeks . org/get-n-最大值-来自熊猫中的特定列-dataframe/](https://www.geeksforgeeks.org/get-n-largest-values-from-a-particular-column-in-pandas-dataframe/)

[Pandas DataFrame](https://www.geeksforgeeks.org/python-pandas-dataframe/) 是一个二维可变大小、潜在异构的表格数据结构，带有标记轴(行和列)。

让我们看看如何从熊猫数据框的特定列中获取 n 个最大值。

首先观察这个数据集。我们将使用该数据的“年龄”、“体重”和“工资”列，以便从熊猫数据框的特定列中获得最大的值。

```py
# importing pandas module 
import pandas as pd 

# making data frame 
df = pd.read_csv("https://media.geeksforgeeks.org/wp-content/uploads/nba.csv") 

df.head(10)
```

![](img/226e9e8f64806663ac99a6ec9423a6c6.png)

**代码#1:** 获得 5 个最大年龄

```py
# importing pandas module 
import pandas as pd 

# making data frame 
df = pd.read_csv("nba.csv") 

# five largest values in column age
df.nlargest(5, ['Age'])
```

**输出:**
![](img/3208b7d4d13b59d32a1fa7e05980911f.png)

**代码#2:** 获得 10 个最大重量

```py
# importing pandas module 
import pandas as pd 

# making data frame 
df = pd.read_csv("nba.csv") 

# Ten largest values in column Weight
df.nlargest(10, ['Weight'])
```

**输出:**
![](img/ba9d12d3848e51c871e40646e90d3ddb.png)

**代码#3:** 获得 10 点最高工资

```py
# importing pandas module 
import pandas as pd 

# making data frame 
df = pd.read_csv("nba.csv") 

# five largest values in column Salary
df.nlargest(5, ['Salary'])
```

**输出:**
![](img/bf39da2058f02e561f5e796f36368813.png)
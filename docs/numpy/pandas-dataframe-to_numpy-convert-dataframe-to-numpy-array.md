# 熊猫 Dataframe . to _ numpy()–将 data frame 转换为 Numpy 数组

> 原文:[https://www . geesforgeks . org/pandas-data frame-to _ numpy-convert-data frame-to-numpy-array/](https://www.geeksforgeeks.org/pandas-dataframe-to_numpy-convert-dataframe-to-numpy-array/)

[Pandas DataFrame](https://www.geeksforgeeks.org/python-pandas-dataframe/) 是一个二维可变大小、潜在异构的表格数据结构，带有标记轴(行和列)。借助 **Dataframe.to_numpy()** 方法，可以将该数据结构转换为 NumPy 数组。

> **语法:** Dataframe.to_numpy(dtype =无，copy = False)
> 
> **参数:**
> **数据类型:**我们像字符串一样传递的数据类型。
> **复制:**【bool，默认值 False】确保返回值不是另一个数组上的视图。
> 
> **返回:**
> numpy.ndarray

要获得 csv 文件的链接，点击 [nba.csv](https://media.geeksforgeeks.org/wp-content/uploads/nba.csv)

**示例 1:** 使用方法`DataFrame.to_numpy()`将数据帧更改为 numpy 数组。永远记住，当处理大量数据时，你应该首先清理数据，以获得高精度。虽然在这段代码中，我们使用`.head()`方法使用了权重列的前五个值。

```
# importing pandas
import pandas as pd 

# reading the csv  
data = pd.read_csv("nba.csv") 

data.dropna(inplace = True)

# creating DataFrame form weight column
gfg = pd.DataFrame(data['Weight'].head())

# using to_numpy() function
print(gfg.to_numpy())
```

**输出:**

```
[[180.]
 [235.]
 [185.]
 [235.]
 [238.]]
```

**示例 2:** 在这段代码中，我们只是在同一个代码中给出了参数。所以我们在这里提供了数据类型。

```
# importing pandas
import pandas as pd 

# read csv file  
data = pd.read_csv("nba.csv") 

data.dropna(inplace = True)

# creating DataFrame form weight column
gfg = pd.DataFrame(data['Weight'].head())

# providing dtype
print(gfg.to_numpy(dtype ='float32'))
```

**输出:**

```
[[180.]
 [235.]
 [185.]
 [235.]
 [238.]]
```

**示例 3:** 验证转换后数组的类型。

```
# importing pandas 
import pandas as pd 

# reading csv  
data = pd.read_csv("nba.csv") 

data.dropna(inplace = True)

# creating DataFrame form weight column
gfg = pd.DataFrame(data['Weight'].head())

# using to_numpy()
print(type(gfg.to_numpy()))
```

**输出:**

```
<class 'numpy.ndarray'>
```
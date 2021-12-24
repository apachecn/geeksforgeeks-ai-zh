# Python | Pandas series . to _ numpy()

> 原文:[https://www . geesforgeks . org/python-pandas-series-to _ numpy/](https://www.geeksforgeeks.org/python-pandas-series-to_numpy/)

**Pandas Series.to_numpy()** 函数用于返回一个 numpy 数组，该数组代表给定系列或索引中的值。

这个功能将解释我们如何将熊猫**系列**转换成数字**阵列**。虽然很简单，但是这种手法背后的概念非常独特。因为我们知道数列在输出中有索引。而在 numpy 数组中，我们只有 numpy 数组中的元素。

> **语法:** Series.to_numpy()
> 
> **参数:**
> **数据类型:**我们像字符串一样传递的数据类型。
> **复制:**【bool，默认值 False】确保返回值不是另一个数组上的视图。

要获得 csv 文件的链接，点击 [nba.csv](https://media.geeksforgeeks.org/wp-content/uploads/nba.csv)

**代码#1 :**

使用方法`Series.to_numpy()`将系列变为*数字阵列*。永远记住，当处理大量数据时，你应该首先清理数据，以获得高精度。虽然在本代码中，我们通过使用`.head()`方法使用了**权重**列的前五个值。

```py
# importing pandas
import pandas as pd 

# reading the csv  
data = pd.read_csv("nba.csv") 

data.dropna(inplace = True)

# creating series form weight column
gfg = pd.Series(data['Weight'].head())

# using to_numpy() function
print(type(gfg.to_numpy()))
```

**输出:**

```py
[180\. 235\. 185\. 235\. 238.]

```

**代码#2 :**
在这段代码中，我们只是在同一个代码中给出了参数。所以我们在这里提供**数据类型**。

```py
# importing pandas
import pandas as pd 

# read csv file  
data = pd.read_csv("nba.csv") 

data.dropna(inplace = True)

# creating series form weight column
gfg = pd.Series(data['Weight'].head())

# providing dtype
print(gfg.to_numpy(dtype ='float32'))
```

**输出:**

```py
[180\. 235\. 185\. 235\. 238.]

```

**代码#3 :** 验证转换后数组的类型。

```py
# importing pandas 
import pandas as pd 

# reading csv  
data = pd.read_csv("nba.csv") 

data.dropna(inplace = True)

# creating series form weight column
gfg = pd.Series(data['Weight'].head())

# using to_numpy()
print(type(gfg.to_numpy()))
```

**输出:**

```py
<class 'numpy.ndarray'>

```
# 如何获取第一排熊猫数据帧？

> 原文:[https://www . geesforgeks . org/如何获得第一排熊猫-dataframe/](https://www.geeksforgeeks.org/how-to-get-first-row-of-pandas-dataframe/)

在本文中，我们将讨论如何获得熊猫数据帧的第一行

## 方法 1:使用 [iloc[]](https://www.geeksforgeeks.org/python-extracting-rows-using-pandas-iloc/)

此方法用于通过使用行号来访问行。我们可以通过使用 0 个索引来获得第一行。

**语法**:

```py
dataframe.iloc[0]
```

其中数据帧是输入数据帧

我们也可以提供范围指数。

**语法:**

```py
dataframe.iloc[:1]
```

在这里，行将从开始提取，直到索引-1 出现在:。

**示例** : Python 代码使用 iloc[]函数

## Python 3

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

# get first row using row position
print(data.iloc[0])

print("---------------")

# get first row using slice operator
print(data.iloc[:1])
```

获取数据帧的第一行

**输出** :

```py
id            7058
name        sravan
subjects      java
Name: 0, dtype: object
---------------
     id    name subjects
0  7058  sravan     java
```

**示例 2:** 获取特定列的第一行

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

# get first row using row position
print(data['name'].iloc[0])

print("---------------")

# get first row using slice operator
print(data['subjects'].iloc[:1])
```

**输出:**

```py
sravan
---------------
0    java
Name: subjects, dtype: object
```

## 方法二:使用[头()](https://www.geeksforgeeks.org/python-pandas-dataframe-series-head-method/)功能

该函数将默认返回数据帧的前 5 行。为了只得到第一行，我们必须指定 1

**语法** :

```py
dataframe.head(1)
```

**示例 1** :程序获取数据集第一行

## python 3

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

# get first row using head() function
print(data.head(1))
```

**输出** :

```py
 id    name subjects
0  7058  sravan     java
```

**示例 2:** 获取特定列的第一行

## python 3

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

# get first row using head() function
print(data['id'].head(1))
```

**输出:**

```py
0    7058
Name: id, dtype: int64
```

## 方法三:使用 [loc()](https://www.geeksforgeeks.org/python-pandas-dataframe-loc/) 功能

此方法用于获取带有索引函数的第一行。

**语法** :

```py
dataframe.loc[dataframe.index[0]]
```

其中，

*   A data frame is an input data frame.
*   Index is to get the first row.

的函数

**示例**:程序获取数据集的第一行

## python 3

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

# get first row using loc() function
data.loc[data.index[0]]
```

**输出:**

```py
id            7058
name        sravan
subjects      java
Name: 0, dtype: object
```

## 方法 4:使用 values()函数

这将以数组的形式返回第一行。工作方式类似于 iloc()。

**语法** :

```py
dataframe.values[0]
```

```py
dataframe.values[:1]
```

**示例**:程序获取数据集第一行

## python 3

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

# get first row using loc() function
print(data.values[:1])

# get first row using loc() function
print(data.values[:1])

# get particular column
print(data['name'].values[:1])
```
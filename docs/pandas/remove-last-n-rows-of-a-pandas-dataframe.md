# 删除熊猫数据框的最后 n 行

> 原文:[https://www . geesforgeks . org/remove-最后 n 行熊猫-dataframe/](https://www.geeksforgeeks.org/remove-last-n-rows-of-a-pandas-dataframe/)

让我们看看删除熊猫数据框最后 n 行的各种方法。
首先，让我们制作一个数据框架:

## 蟒蛇 3

```py
# Import Required Libraries
import pandas as pd

# Create a dictionary for the dataframe
dict = {
  'Name': ['Sukritin', 'Sumit Tyagi', 'Akriti Goel',
           'Sanskriti', 'Abhishek Jain'],
  'Age': [22, 20, 45, 21, 22],
   'Marks': [90, 84, -33, -87, 82]
}

# Converting Dictionary to
# Pandas Dataframe
df = pd.DataFrame(dict)

# Print Dataframe
print(df)
```

**输出:**

![](img/697307573ff7afc85171c07d85319da9.png)

**方法 1:** 使用 [**Dataframe.drop()**](https://www.geeksforgeeks.org/python-delete-rows-columns-from-dataframe-using-pandas-drop/) 。
我们可以使用 drop()方法删除最后 n 行。drop()方法获取一个带布尔值的 inplace 参数。如果 inplace 属性设置为 True，则数据框将使用数据框的新值进行更新(删除最后 n 行的数据框)。

**示例:**

## 蟒蛇 3

```py
# Import Required Libraries
import pandas as pd

# Create a dictionary for the dataframe
dict = {
  'Name': ['Sukritin', 'Sumit Tyagi', 'Akriti Goel',
           'Sanskriti', 'Abhishek Jain'],
  'Age': [22, 20, 45, 21, 22],
   'Marks': [90, 84, -33, -87, 82]
}

# Converting Dictionary to
# Pandas Dataframe
df = pd.DataFrame(dict)

# Number of rows to drop
n = 3

# Dropping last n rows using drop
df.drop(df.tail(n).index,
        inplace = True)

# Printing dataframe
print(df)
```

**输出:**

![](img/6802597565b4f88c27f4a3e3cd55851b.png)

**方法二:**使用**[**data frame . iloc[]**](https://www.geeksforgeeks.org/python-extracting-rows-using-pandas-iloc/)**。****

**当数据帧的索引标签不是 0、1、2、3 的数字序列时，使用这个方法。或者在用户不知道索引标签的情况下。**

****示例:****

## **蟒蛇 3**

```py
# Import Required Libraries
import pandas as pd

# Create a dictionary for the dataframe
dict = {
  'Name': ['Sukritin', 'Sumit Tyagi', 'Akriti Goel',
           'Sanskriti', 'Abhishek Jain'],
  'Age': [22, 20, 45, 21, 22],
   'Marks': [90, 84, -33, -87, 82]
}

# Converting Dictionary to
# Pandas Dataframe
df = pd.DataFrame(dict)

# Number of rows to drop
n = 3

# Removing last n rows
df_dropped_last_n = df.iloc[:-n]

# Printing dataframe
print(df_dropped_last_n)
```

****输出:****

**![](img/6802597565b4f88c27f4a3e3cd55851b.png)**

****方法三:**使用**[**data frame . head()**](https://www.geeksforgeeks.org/python-pandas-dataframe-series-head-method/)**。******

****此方法用于返回数据框或系列的前 n 行(默认为 5 行)。****

******示例:******

## ****蟒蛇 3****

```py
**# Import Required Libraries
import pandas as pd

# Create a dictionary for the dataframe
dict = {
  'Name': ['Sukritin', 'Sumit Tyagi', 'Akriti Goel',
           'Sanskriti', 'Abhishek Jain'],
  'Age': [22, 20, 45, 21, 22],
   'Marks': [90, 84, -33, -87, 82]
}

# Converting Dictionary to
# Pandas Dataframe
df = pd.DataFrame(dict)

# Number of rows to drop
n = 3

# Using head() to
# drop last n rows
df1 = df.head(-n)

# Printing dataframe
print(df1)**
```

******输出:******

****![](img/6802597565b4f88c27f4a3e3cd55851b.png)****

******方法 4:** 使用**数据帧切片[ ]。******

******示例:******

## ****蟒蛇 3****

```py
**# Import Required Libraries
import pandas as pd

# Create a dictionary for the dataframe
dict = {
  'Name': ['Sukritin', 'Sumit Tyagi', 'Akriti Goel',
           'Sanskriti', 'Abhishek Jain'],
  'Age': [22, 20, 45, 21, 22],
   'Marks': [90, 84, -33, -87, 82]
}

# Converting Dictionary to
# Pandas Dataframe
df = pd.DataFrame(dict)

# Number of rows to drop
n = 3

# Slicing last n rows
df1 = df[:-n]

# Printing dataframe
print(df1)**
```

******输出:****** 

****![](img/6802597565b4f88c27f4a3e3cd55851b.png)****
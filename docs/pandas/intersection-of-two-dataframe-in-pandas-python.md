# 熊猫中两个数据框的交集–Python

> 原文:[https://www . geesforgeks . org/熊猫数据框交集-python/](https://www.geeksforgeeks.org/intersection-of-two-dataframe-in-pandas-python/)

使用预定义函数 **`merge()`** ，可以轻松计算熊猫中两个数据帧的交集。该函数将两个数据框都作为参数，并返回它们之间的交集。

**语法:**

```py
pd.merge(df1, df2, how)
```

**例 1:**

```py
import pandas as pd

# Creating Data frames
df1 = {'A': [1, 2, 3, 4],
         'B': ['abc', 'def', 'efg', 'ghi']} 
df2 = {'A': [1, 2, 3, 4 ],
         'B': ['Geeks', 'For', 'efg', 'ghi'],
         'C':['Nikhil', 'Rishabh', 'Rahul', 'Shubham']} 

d1 = pd.DataFrame(df1)
d2 = pd.DataFrame(df2) 

# Calling merge() function
int_df = pd.merge(d1, d2, how ='inner', on =['A', 'B'])
print(int_df)
```

**输出:**

```py
   A    B        C
0  3  efg    Rahul
1  4  ghi  Shubham

```

**例 2:**

```py
import pandas as pd

# Creating Data frames
df1 = {'A': [1, 2, 3, 4],
         'B': ['Geeks', 'For', 'efg', 'ghi']} 
df2 = {'A': [1, 2, 3, 4 ],
         'B': ['Geeks', 'For', 'abc', 'cde'],
         'C':['Nikhil', 'Rishabh', 'Rahul', 'Shubham']} 

d1 = pd.DataFrame(df1)
d2 = pd.DataFrame(df2) 

# Calling merge() function
int_df = pd.merge(d1, d2, how='inner', on=['A', 'B'])
print(int_df)
```

**输出:**

```py
   A      B        C
0  1  Geeks   Nikhil
1  2    For  Rishabh

```
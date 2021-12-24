# 使用 for 循环

创建熊猫列

> 原文:[https://www . geesforgeks . org/create-a-pandas-column-use-for-loop/](https://www.geeksforgeeks.org/create-a-pandas-column-using-for-loop/)

让我们看看如何使用 for 循环在 pandas dataframe 中创建一个列。当我们需要处理之前为此目的创建的数据帧的数据时，有时需要这样的操作，我们需要这种类型的计算，这样我们就可以处理现有的数据，并创建一个单独的列来存储数据。

这可以通过 for-loop 轻松完成。列的数据可以从现有的数据框或任何数组中获取。

```
# importing libraries
import pandas as pd
import numpy as np

raw_Data = {'Voter_name': ['Geek1', 'Geek2', 'Geek3', 'Geek4', 
                           'Geek5', 'Geek6', 'Geek7', 'Geek8'], 
            'Voter_age': [15, 23, 25, 9, 67, 54, 42, np.NaN]}

df = pd.DataFrame(raw_Data, columns = ['Voter_name', 'Voter_age'])
#       //DataFrame will look like
#
# Voter_name          Voter_age
# Geek1                15
# Geek2                23
# Geek3                25
# Geek4                09
# Geek5                67
# Geek6                54
# Geek7                42
# Geek8           not a number

eligible = []

# For each row in the column
for age in df['Voter_age']:       
    if age >= 18:                   # if Voter eligible
        eligible.append('Yes')
    elif age < 18:                  # if voter is not eligible
        eligible.append("No")
    else:
        eligible.append("Not Sure")

# Create a column from the list
df['Voter'] = eligible  

print(df)
```

**Output:**

```
    Voter_name  Voter_age     Voter
0      Geek1         15        No
1      Geek2         23       Yes
2      Geek3         25       Yes
3      Geek4          9        No
4      Geek5         67       Yes
5      Geek6         54       Yes
6      Geek7         42       Yes
7      Geek8        NaN  Not Sure

```
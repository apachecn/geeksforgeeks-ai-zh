# 使用熊猫

中的 iloc[]和 iat[]从数据框中选择任意一行

> 原文:[https://www . geesforgeks . org/从数据框中选择任意行-使用-iloc-and-iat-in-pandas/](https://www.geeksforgeeks.org/select-any-row-from-a-dataframe-using-iloc-and-iat-in-pandas/)

在本文中，我们将学习如何使用函数 ilic[]和 iat[]从数据框中获取列表行。有多种方法可以从给定的数据框中获取列表形式的行。让我们看看他们会不会借助例子。

## 计算机编程语言

```
import pandas as pd

# Create the dataframe
df = pd.DataFrame({'Date':['10/2/2011', '11/2/2011', '12/2/2011', '13/2/11'],
                    'Event':['Music', 'Poetry', 'Theatre', 'Comedy'],
                    'Cost':[10000, 5000, 15000, 2000]})

# Create an empty list
Row_list =[]

# Iterate over each row
for i in range((df.shape[0])):

    # Using iloc to access the values of 
    # the current row denoted by "i"
    Row_list.append(list(df.iloc[i, :]))

# Print the first 3 elements
print(Row_list[:3])
```

**输出:**

```
[[10000, '10/2/2011', 'Music'], [5000, '11/2/2011', 'Poetry'],
      [15000, '12/2/2011', 'Theatre']
```

**使用 iat[]方法–**

## 蟒蛇 3

```
# importing pandas as pd
import pandas as pd

# Create the dataframe
df = pd.DataFrame({'Date':['10/2/2011', '11/2/2011', '12/2/2011', '13/2/11'],
                    'Event':['Music', 'Poetry', 'Theatre', 'Comedy'],
                    'Cost':[10000, 5000, 15000, 2000]})

# Create an empty list
Row_list =[]

# Iterate over each row
for i in range((df.shape[0])):
    # Create a list to store the data
    # of the current row
    cur_row =[]

    # iterate over all the columns
    for j in range(df.shape[1]):

        # append the data of each
        # column to the list
        cur_row.append(df.iat[i, j])

    # append the current row to the list
    Row_list.append(cur_row)

# Print the first 3 elements
print(Row_list[:3])
```

**输出:**

```
[[10000, '10/2/2011', 'Music'], [5000, '11/2/2011', 'Poetry'], 
      [15000, '12/2/2011', 'Theatre']]
```
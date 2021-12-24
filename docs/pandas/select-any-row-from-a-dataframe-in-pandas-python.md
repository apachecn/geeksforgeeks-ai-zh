# 从熊猫| Python 的数据框中选择任意一行

> 原文:[https://www . geesforgeks . org/从熊猫数据框中选择任意行-python/](https://www.geeksforgeeks.org/select-any-row-from-a-dataframe-in-pandas-python/)

在本文中，我们将学习如何以列表的形式从数据框中获取行，而不使用像 ilic[]这样的函数。有多种方法可以从给定的数据框中获取列表形式的行。让我们看看他们会不会借助例子。

```
# importing pandas as pd 
import pandas as pd 

# Create the dataframe 
df = pd.DataFrame({'Date':['10/2/2011', '11/2/2011', '12/2/2011', '13/2/11'], 
                    'Event':['Music', 'Poetry', 'Theatre', 'Comedy'], 
                    'Cost':[10000, 5000, 15000, 2000]}) 

# using interrors() method

# Create an empty list 
Row_list =[] 

# Iterate over each row 
for index, rows in df.iterrows(): 

    # Create list for the current row 
    my_list =[rows.Date, rows.Event, rows.Cost] 

    # append the list to the final list 
    Row_list.append(my_list) 

# Print the list 
print(Row_list) 
```

**输出:**

```
[['10/2/2011', 'Music', 10000], ['11/2/2011', 'Poetry', 5000], 
      ['12/2/2011', 'Theatre', 15000], ['13/2/11', 'Comedy', 2000]]

```

```

# Print the first 2 elements 
print(Row_list[:2]) 
```

**输出:**

```
[['10/2/2011', 'Music', 10000], ['11/2/2011', 'Poetry', 5000]]

```
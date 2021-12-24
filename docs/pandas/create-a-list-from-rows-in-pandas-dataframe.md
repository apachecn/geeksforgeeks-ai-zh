# 根据熊猫数据框中的行创建列表

> 原文:[https://www . geeksforgeeks . org/create-a-list-from-row-in-pandas-data frame/](https://www.geeksforgeeks.org/create-a-list-from-rows-in-pandas-dataframe/)

Python 列表很容易使用，而且 list 有很多内置函数，可以对列表进行大量操作。熊猫数据框的列由系列组成，但与列不同，熊猫数据框的行没有任何相似的关联。在这篇文章中，我们将讨论几种一次提取整行数据帧的方法。

**解决方案#1:** 为了迭代熊猫数据帧的行，我们可以使用`DataFrame.iterrows()`函数，然后我们可以将每行的数据附加到列表的末尾。

```py
# importing pandas as pd
import pandas as pd

# Create the dataframe
df = pd.DataFrame({'Date':['10/2/2011', '11/2/2011', '12/2/2011', '13/2/11'],
                    'Event':['Music', 'Poetry', 'Theatre', 'Comedy'],
                    'Cost':[10000, 5000, 15000, 2000]})

# Print the dataframe
print(df)
```

**输出:**

![](img/4812770ba9593ee9be742b556467470f.png)

现在，我们将使用`DataFrame.iterrows()`函数迭代给定数据帧的每一行，并根据每一行的数据构建一个列表。

```py
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

![](img/063937bf7626e899e952ca87e872e5c6.png)

正如我们在输出中看到的，我们已经成功地将给定数据帧的每一行提取到一个列表中。就像任何其他 Python 的列表一样，我们可以对提取的列表执行任何列表操作。

```py
# Find the length of the newly 
# created list
print(len(Row_list))

# Print the first 3 elements
print(Row_list[:3])
```

**输出:**

![](img/f2df1c74f371767e715794dc5777e1a4.png)

![](img/a7d46a94f54366f24f32c288a978b0b5.png)

**解决方案#2:** 为了迭代熊猫数据帧的行，我们可以使用`DataFrame.itertuples()`函数，然后我们可以将每行的数据附加到列表的末尾。

```py
# importing pandas as pd
import pandas as pd

# Create the dataframe
df = pd.DataFrame({'Date':['10/2/2011', '11/2/2011', '12/2/2011', '13/2/11'],
                    'Event':['Music', 'Poetry', 'Theatre', 'Comedy'],
                    'Cost':[10000, 5000, 15000, 2000]})

# Print the dataframe
print(df)
```

**输出:**

![](img/4812770ba9593ee9be742b556467470f.png)

现在，我们将使用`DataFrame.itertuples()`函数迭代给定数据帧的每一行，并根据每一行的数据构建一个列表。

```py
# Create an empty list
Row_list =[]

# Iterate over each row
for rows in df.itertuples():
    # Create list for the current row
    my_list =[rows.Date, rows.Event, rows.Cost]

    # append the list to the final list
    Row_list.append(my_list)

# Print the list
print(Row_list)
```

**输出:**

![](img/063937bf7626e899e952ca87e872e5c6.png)

正如我们在输出中看到的，我们已经成功地将给定数据帧的每一行提取到一个列表中。就像任何其他 Python 的列表一样，我们可以对提取的列表执行任何列表操作。

```py
# Find the length of the newly 
# created list
print(len(Row_list))

# Print the first 3 elements
print(Row_list[:3])
```

**输出:**

![](img/f2df1c74f371767e715794dc5777e1a4.png)

![](img/a7d46a94f54366f24f32c288a978b0b5.png)
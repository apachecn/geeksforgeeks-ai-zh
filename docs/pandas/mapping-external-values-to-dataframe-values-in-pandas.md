# 将外部值映射到熊猫的数据帧值

> 原文:[https://www . geesforgeks . org/mapping-external-values-to-data frame-values-in-pandas/](https://www.geeksforgeeks.org/mapping-external-values-to-dataframe-values-in-pandas/)

将外部值映射到数据框意味着通过保持外部字典的键与该数据框的一列相同，使用不同的值集添加到该数据框中。

要在数据框中添加外部值，我们使用字典，该字典包含要添加到数据框中的键和值。通过在数据框中添加外部值，一列将被添加到当前数据框中。在熊猫的帮助下，我们还可以将一个数据帧映射或组合到其他数据帧。

**方法#1:** 使用映射函数

通过使用这个映射函数，我们可以向现有的数据框中再添加一列。请记住，任何键值都不会重复，这将使数据不一致。

```py
# Creating new dataframe
import pandas as pd

initial_data = {'First_name': ['Ram', 'Mohan', 'Tina', 'Jeetu', 'Meera'], 
        'Last_name': ['Kumar', 'Sharma', 'Ali', 'Gandhi', 'Kumari'], 
        'Age': [42, 52, 36, 21, 23], 
        'City': ['Mumbai', 'Noida', 'Pune', 'Delhi', 'Bihar']}

df = pd.DataFrame(initial_data, columns = ['First_name', 'Last_name',
                                                      'Age', 'City'])

# Create new column using dictionary
new_data = { "Ram":"B.Com",
             "Mohan":"IAS",
             "Tina":"LLB",
             "Jeetu":"B.Tech",
             "Meera":"MBBS" }

# combine this new data with existing DataFrame
df["Qualification"] = df["First_name"].map(new_data)

print(df)
```

**Output:**

```py
First_name Last_name  Age    City    Qualification
0        Ram     Kumar   42  Mumbai         B.Com
1      Mohan    Sharma   52   Noida           IAS
2       Tina       Ali   36    Pune           LLB
3      Jeetu    Gandhi   21   Delhi        B.Tech
4      Meera    Kumari   23   Bihar          MBBS

```

**方法 2:** 使用`replace` 功能

在这种方法中，我们可以用一些定义的外部值来添加或替换数据帧的一些值。

```py
# Creating new dataframe
import pandas as pd
initial_data = {'First_name': ['Ram', 'Mohan', 'Tina', 'Jeetu', 'Meera'], 
                'Last_name': ['Kumar', 'Sharma', 'Ali', 'Gandhi', 'Kumari'], 
                'Age': [42, 52, 36, 21, 23], 
                'City': ['Mumbai', 'Noida', 'Pune', 'Delhi', 'Bihar']}

df = pd.DataFrame(initial_data, columns = ['First_name', 'Last_name',
                                                      'Age', 'City'])

# Create new column using dictionary
new_data = { "Ram":"Shyam",
             "Tina":"Riya",
             "Jeetu":"Jitender" }

print(df, end ="\n\n")

# combine this new data with existing DataFrame
df = df.replace({"First_name":new_data})
print(df)
```

**Output:**

```py
First_name Last_name  Age    City
0        Ram     Kumar   42  Mumbai
1      Mohan    Sharma   52   Noida
2       Tina       Ali   36    Pune
3      Jeetu    Gandhi   21   Delhi
4      Meera    Kumari   23   Bihar

  First_name Last_name  Age    City
0      Shyam     Kumar   42  Mumbai
1      Mohan    Sharma   52   Noida
2       Riya       Ali   36    Pune
3   Jitender    Gandhi   21   Delhi
4      Meera    Kumari   23   Bihar

```

**方法#3:** 使用`update` 功能

在这种方法中，我们可以通过使用索引值来更新 dataframe 值，我们可以通过外部数据来更改列的值。

```py
# Creating new dataframe
import pandas as pd

initial_data = {'First_name': ['Ram', 'Mohan', 'Tina', 'Jeetu', 'Meera'], 
                'Last_name': ['Kumar', 'Sharma', 'Ali', 'Gandhi', 'Kumari'], 
                'Age': [42, 52, 36, 21, 23], 
                'City': ['Mumbai', 'Noida', 'Pune', 'Delhi', 'Bihar']}

df = pd.DataFrame(initial_data, columns = ['First_name', 'Last_name',
                                                      'Age', 'City'])

# Create new column using dictionary
new_data = { 0:"Shyam",
             2:"Riya",
             3:"Jitender" }

# combine this new data with existing DataFrame
df["First_name"].update(pd.Series(new_data))
print(df)
```

**Output:**

```py
First_name Last_name  Age    City
0      Shyam     Kumar   42  Mumbai
1      Mohan    Sharma   52   Noida
2       Riya       Ali   36    Pune
3   Jitender    Gandhi   21   Delhi
4      Meera    Kumari   23   Bihar

```
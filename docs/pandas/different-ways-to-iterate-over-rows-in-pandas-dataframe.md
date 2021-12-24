# 在熊猫数据框中迭代行的不同方式

> 原文:[https://www . geeksforgeeks . org/不同的迭代方式-熊猫中的行-数据框/](https://www.geeksforgeeks.org/different-ways-to-iterate-over-rows-in-pandas-dataframe/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 Python 包的奇妙生态系统。**熊猫**就是其中的一个包，让导入和分析数据变得更加容易。

让我们看看熊猫**数据框**中迭代行的不同方法:

**方法#1 :** 使用数据框的**索引**属性。

```py
# import pandas package as pd
import pandas as pd

# Define a dictionary containing students data
data = {'Name': ['Ankit', 'Amit', 'Aishwarya', 'Priyanka'],
                'Age': [21, 19, 20, 18],
                'Stream': ['Math', 'Commerce', 'Arts', 'Biology'],
                'Percentage': [88, 92, 95, 70]}

# Convert the dictionary into DataFrame
df = pd.DataFrame(data, columns = ['Name', 'Age', 'Stream', 'Percentage'])

print("Given Dataframe :\n", df)

print("\nIterating over rows using index attribute :\n")

# iterate through each row and select 
# 'Name' and 'Stream' column respectively.
for ind in df.index:
     print(df['Name'][ind], df['Stream'][ind])
```

**Output:**

```py
Given Dataframe :
         Name  Age    Stream  Percentage
0      Ankit   21      Math          88
1       Amit   19  Commerce          92
2  Aishwarya   20      Arts          95
3   Priyanka   18   Biology          70

Iterating over rows using index attribute :

Ankit Math
Amit Commerce
Aishwarya Arts
Priyanka Biology

```

**方法 2 :** 使用数据框的**loc【】**功能。

```py
# import pandas package as pd
import pandas as pd

# Define a dictionary containing students data
data = {'Name': ['Ankit', 'Amit', 'Aishwarya', 'Priyanka'],
                'Age': [21, 19, 20, 18],
                'Stream': ['Math', 'Commerce', 'Arts', 'Biology'],
                'Percentage': [88, 92, 95, 70]}

# Convert the dictionary into DataFrame
df = pd.DataFrame(data, columns = ['Name', 'Age', 'Stream', 'Percentage'])

print("Given Dataframe :\n", df)

print("\nIterating over rows using loc function :\n")

# iterate through each row and select 
# 'Name' and 'Age' column respectively.
for i in range(len(df)) :
  print(df.loc[i, "Name"], df.loc[i, "Age"])
```

**Output:**

```py
Given Dataframe :
         Name  Age    Stream  Percentage
0      Ankit   21      Math          88
1       Amit   19  Commerce          92
2  Aishwarya   20      Arts          95
3   Priyanka   18   Biology          70

Iterating over rows using loc function :

Ankit 21
Amit 19
Aishwarya 20
Priyanka 18

```

**方法#3 :** 使用数据框的**iloc【】**功能。

```py
# import pandas package as pd
import pandas as pd

# Define a dictionary containing students data
data = {'Name': ['Ankit', 'Amit', 'Aishwarya', 'Priyanka'],
                'Age': [21, 19, 20, 18],
                'Stream': ['Math', 'Commerce', 'Arts', 'Biology'],
                'Percentage': [88, 92, 95, 70]}

# Convert the dictionary into DataFrame
df = pd.DataFrame(data, columns = ['Name', 'Age', 'Stream', 'Percentage'])

print("Given Dataframe :\n", df)

print("\nIterating over rows using iloc function :\n")

# iterate through each row and select 
# 0th and 2nd index column respectively.
for i in range(len(df)) :
  print(df.iloc[i, 0], df.iloc[i, 2])
```

**Output:**

```py
Given Dataframe :
         Name  Age    Stream  Percentage
0      Ankit   21      Math          88
1       Amit   19  Commerce          92
2  Aishwarya   20      Arts          95
3   Priyanka   18   Biology          70

Iterating over rows using iloc function :

Ankit Math
Amit Commerce
Aishwarya Arts
Priyanka Biology

```

**方法#4 :** 使用数据框的**ITER row()**方法。

```py
# import pandas package as pd
import pandas as pd

# Define a dictionary containing students data
data = {'Name': ['Ankit', 'Amit', 'Aishwarya', 'Priyanka'],
                'Age': [21, 19, 20, 18],
                'Stream': ['Math', 'Commerce', 'Arts', 'Biology'],
                'Percentage': [88, 92, 95, 70]}

# Convert the dictionary into DataFrame
df = pd.DataFrame(data, columns = ['Name', 'Age', 'Stream', 'Percentage'])

print("Given Dataframe :\n", df)

print("\nIterating over rows using iterrows() method :\n")

# iterate through each row and select 
# 'Name' and 'Age' column respectively.
for index, row in df.iterrows():
    print (row["Name"], row["Age"])
```

**Output:**

```py
Given Dataframe :
         Name  Age    Stream  Percentage
0      Ankit   21      Math          88
1       Amit   19  Commerce          92
2  Aishwarya   20      Arts          95
3   Priyanka   18   Biology          70

Iterating over rows using iterrows() method :

Ankit 21
Amit 19
Aishwarya 20
Priyanka 18

```

**方法#5 :** 使用数据框的 **itertuples()** 方法。

```py
# import pandas package as pd
import pandas as pd

# Define a dictionary containing students data
data = {'Name': ['Ankit', 'Amit', 'Aishwarya', 'Priyanka'],
                'Age': [21, 19, 20, 18],
                'Stream': ['Math', 'Commerce', 'Arts', 'Biology'],
                'Percentage': [88, 92, 95, 70]}

# Convert the dictionary into DataFrame
df = pd.DataFrame(data, columns = ['Name', 'Age', 'Stream', 'Percentage'])

print("Given Dataframe :\n", df)

print("\nIterating over rows using itertuples() method :\n")

# iterate through each row and select 
# 'Name' and 'Percentage' column respectively.
for row in df.itertuples(index = True, name ='Pandas'):
    print (getattr(row, "Name"), getattr(row, "Percentage"))
```

**Output:**

```py
Given Dataframe :
         Name  Age    Stream  Percentage
0      Ankit   21      Math          88
1       Amit   19  Commerce          92
2  Aishwarya   20      Arts          95
3   Priyanka   18   Biology          70

Iterating over rows using itertuples() method :

Ankit 88
Amit 92
Aishwarya 95
Priyanka 70

```

**方法#6 :** 使用**应用()**方法的数据框。

```py
# import pandas package as pd
import pandas as pd

# Define a dictionary containing students data
data = {'Name': ['Ankit', 'Amit', 'Aishwarya', 'Priyanka'],
                'Age': [21, 19, 20, 18],
                'Stream': ['Math', 'Commerce', 'Arts', 'Biology'],
                'Percentage': [88, 92, 95, 70]}

# Convert the dictionary into DataFrame
df = pd.DataFrame(data, columns = ['Name', 'Age', 'Stream', 'Percentage'])

print("Given Dataframe :\n", df)

print("\nIterating over rows using apply function :\n")

# iterate through each row and concatenate
# 'Name' and 'Percentage' column respectively.
print(df.apply(lambda row: row["Name"] + " " + str(row["Percentage"]), axis = 1))
```

**Output:**

```py
Given Dataframe :
         Name  Age    Stream  Percentage
0      Ankit   21      Math          88
1       Amit   19  Commerce          92
2  Aishwarya   20      Arts          95
3   Priyanka   18   Biology          70

Iterating over rows using apply function :

0        Ankit 88
1         Amit 92
2    Aishwarya 95
3     Priyanka 70
dtype: object

```
# 在熊猫数据框中排序行

> 原文:[https://www . geeksforgeeks . org/sorting-row-in-pandas-data frame/](https://www.geeksforgeeks.org/sorting-rows-in-pandas-dataframe/)

Pandas DataFrame 是一个二维可变大小的、潜在异构的表格数据结构，带有标签轴(行和列)。在处理数据时，我们经常需要对行和列进行某些操作。

让我们看看如何对熊猫数据框中的行进行排序。

**代码#1:** 按*科学*排序行

```
# import modules
import pandas as pd

# create dataframe
data = {'name': ['Simon', 'Marsh', 'Gaurav', 'Alex', 'Selena'], 
        'Maths': [8, 5, 6, 9, 7], 
        'Science': [7, 9, 5, 4, 7],
        'English': [7, 4, 7, 6, 8]}

df = pd.DataFrame(data)

# Sort the dataframe’s rows by Science,
# in descending order
a = df.sort_values(by ='Science', ascending = 0)
print("Sorting rows by Science:\n \n", a)
```

**Output:**

```
Sorting rows by Science:

    English  Maths  Science    name
1        4      5        9   Marsh
0        7      8        7   Simon
4        8      7        7  Selena
2        7      6        5  Gaurav
3        6      9        4    Alex

```

**代码#2:** 先按数学再按英语对行进行排序。

```
# import modules
import pandas as pd

# create dataframe
data = {'name': ['Simon', 'Marsh', 'Gaurav', 'Alex', 'Selena'], 
        'Maths': [8, 5, 6, 9, 7], 
        'Science': [7, 9, 5, 4, 7],
        'English': [7, 4, 7, 6, 8]}

df = pd.DataFrame(data)

# Sort the dataframe’s rows by Maths
# and then by English, in ascending order
b = df.sort_values(by =['Maths', 'English'])
print("Sort rows by Maths and then by English: \n\n", b)
```

**Output:**

```
Sort rows by Maths and then by English: 

    English  Maths  Science    name
1        4      5        9   Marsh
2        7      6        5  Gaurav
4        8      7        7  Selena
0        7      8        7   Simon
3        6      9        4    Alex

```

**代码#3:** 如果你想先缺值。

```
import pandas as pd

# create dataframe
data = {'name': ['Simon', 'Marsh', 'Gaurav', 'Alex', 'Selena'], 
        'Maths': [8, 5, 6, 9, 7], 
        'Science': [7, 9, 5, 4, 7],
        'English': [7, 4, 7, 6, 8]}
df = pd.DataFrame(data)

a = df.sort_values(by ='Science', na_position ='first' )
print(a)
```

**Output:**

```
English  Maths  Science    name
3        6      9        4    Alex
2        7      6        5  Gaurav
0        7      8        7   Simon
4        8      7        7  Selena
1        4      5        9   Marsh

```

由于本例中没有缺失值，这将产生与上面相同的输出，但按升序排序。
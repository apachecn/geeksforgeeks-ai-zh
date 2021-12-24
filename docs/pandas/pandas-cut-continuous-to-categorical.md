# 熊猫切割–连续到分类

> 原文:[https://www . geesforgeks . org/pandas-cut-continuous-to-classic/](https://www.geeksforgeeks.org/pandas-cut-continuous-to-categorical/)

数据分析中经常会看到连续的、高度倾斜的数据等数字数据。有时，从连续数据转换到离散数据时，分析变得毫不费力。有许多方法可以进行转换，其中一种方法是使用熊猫的综合切割功能。熊猫切割函数是将数值连续数据转换为分类数据的一种独特方式。它有三个主要的必要部分:

1.  首先是输入所需的一维数组/数据帧。
2.  另一个主要部分是垃圾箱。表示连续数据的独立箱的边界的箱。第一个数字表示容器的起点，后面的数字表示容器的终点。切割功能允许更清晰的箱柜
3.  最后的主要部分是标签。标签的数量无一例外地比箱子的数量少一个。

**注意:**对于任何 NA 值，结果将存储为 NA。在结果分类箱中，超出范围的值也将是“不适用”。

在使用 pandas cut 函数时，它无法保证值在每个箱中的分布。事实上，我们最终可能会以这样一种方式定义容器，即容器可能不包含任何值。

> **语法:** pandas.cut(x，bin，right=True，labels=None，retbins = False，precision=3，include _ low = False，duplicates='raise '，ordered=True)
> 
> **参数:**
> 
> *   **x:** 输入数组。需要是一维的。
> *   **面元:**表示分割的面元边界
> *   **右侧:**表示是否应包含箱的最右边。布尔类型的值。默认值为真。
> *   **标签:**定义返回的分段箱的标签。数组或布尔值
> 
> **返回值:**返回分类序列/数值数组/区间索引

**示例 1:** 假设我们有一个由 15 个从 1 到 100 的随机数组成的数组“Age ”,我们希望将数据分成 4 个类别仓–

```
'Baby/Toddler' :- 0 to 3 years
'Child' :- 4 to 17 years
'Adult' :- 18 to 63 years
'Elderly' :- 64 to 99 years
```

## 蟒蛇 3

```
# Importing pandas and numpy libraries
import pandas as pd
import numpy as np

# Creating a dummy DataFrame of 15 numbers randomly
# ranging from 1-100 for age
df = pd.DataFrame({'Age': [42, 15, 67, 55, 1, 29, 75, 89, 4,
                           10, 15, 38, 22, 77]})

# Printing DataFrame Before sorting Continuous 
# to Categories
print("Before: ")
print(df)

# A column of name 'Label' is created in DataFrame
# Categorizing Age into 4 Categories
# Baby/Toddler: (0,3], 0 is excluded & 3 is included
# Child: (3,17], 3 is excluded & 17 is included
# Adult: (17,63], 17 is excluded & 63 is included
# Elderly: (63,99], 63 is excluded & 99 is included
df['Label'] = pd.cut(x=df['Age'], bins=[0, 3, 17, 63, 99],
                     labels=['Baby/Toddler', 'Child', 'Adult',
                             'Elderly'])

# Printing DataFrame after sorting Continuous to
# Categories
print("After: ")
print(df)

# Check the number of values in each bin
print("Categories: ")
print(df['Label'].value_counts())
```

**输出:**

```
Before: 
    Age
0    42
1    15
2    67
3    55
4     1
5    29
6    75
7    89
8     4
9    10
10   15
11   38
12   22
13   77
After: 
    Age         Label
0    42         Adult
1    15         Child
2    67       Elderly
3    55         Adult
4     1  Baby/Toddler
5    29         Adult
6    75       Elderly
7    89       Elderly
8     4         Child
9    10         Child
10   15         Child
11   38         Adult
12   22         Adult
13   77       Elderly
Categories: 
Adult           5
Elderly         4
Child           4
Baby/Toddler    1
Name: Label, dtype: int64
```

**示例#2:** 假设我们有一个 12 人的“高度”数组，从 150 厘米到 180 厘米随机开始，我们希望将数据分成 3 个类别。

```
'Short' :- greater than 150cm upto 157cm
'Average' :- greater than 157cm upto 170cm
'Tall' :- greater than 170cm upto 180cm
```

## 蟒蛇 3

```
# Importing pandas and numpy libraries
import pandas as pd
import numpy as np

# Creating a dummy DataFrame of 12 numbers randomly
# ranging from 150-180 for height
df = pd.DataFrame({'Height': [150.4, 157.6, 170, 176, 164.2, 155,
                              159.2, 175, 162.4, 176, 153, 170.9]})

# Printing DataFrame Before Sorting Continuous to Categories
print("Before: ")
print(df)

# A column of name 'Label' is created in DataFrame
# Categorizing Height into 3 Categories
# Short: (150,157], 150 is excluded & 157 is included
# Average: (157,169], 157 is excluded & 169 is included
# Tall: (169,180], 169 is excluded & 180 is included
df['Label'] = pd.cut(x=df['Height'],
                     bins=[150, 157, 169, 180],
                     labels=['Short', 'Average', 'Tall'])

# Printing DataFrame After Sorting Continuous to Categories
print("After: ")
print(df)

# Check the number of values in each bin
print("Categories: ")
print(df['Label'].value_counts())
```

**输出:**

```
Before: 
    Height
0    150.4
1    157.6
2    170.0
3    176.0
4    164.2
5    155.0
6    159.2
7    175.0
8    162.4
9    176.0
10   153.0
11   170.9
After: 
    Height    Label
0    150.4    Short
1    157.6  Average
2    170.0     Tall
3    176.0     Tall
4    164.2  Average
5    155.0    Short
6    159.2  Average
7    175.0     Tall
8    162.4  Average
9    176.0     Tall
10   153.0    Short
11   170.9     Tall
Categories: 
Tall       5
Average    4
Short      3
Name: Label, dtype: int64
```
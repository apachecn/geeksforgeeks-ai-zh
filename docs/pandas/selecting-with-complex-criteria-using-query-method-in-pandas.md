# 在熊猫中使用查询方法选择复杂条件

> 原文:[https://www . geeksforgeeks . org/复杂条件下的选择使用查询方法熊猫/](https://www.geeksforgeeks.org/selecting-with-complex-criteria-using-query-method-in-pandas/)

在本文中，让我们讨论如何在 Pandas 中使用 Query()方法选择复杂的条件。在使用查询方法选择复杂条件的熊猫中，首先，我们在[熊猫的帮助下创建数据框。Dataframe()](https://www.geeksforgeeks.org/python-pandas-dataframe/) 并将其存储为一个变量，然后借助 [query()](https://www.geeksforgeeks.org/python-filtering-data-with-pandas-query-method/) 方法选择复杂的条件。在[熊猫的帮助下。Dataframe.loc()](https://www.geeksforgeeks.org/python-pandas-dataframe-loc/) 我们可以通过传递数据帧的索引来找到数据帧的细节。
**例 1:**

## 蟒蛇 3

```py
import pandas as pd

df = pd.DataFrame([[10, 20, 30, 40], [70, 14, 21, 80], 
                   [55, 15, 80, 12]],

                  columns=['GFG_USER_1', 'GFG_USER_2',
                           'GFG_USER_3', 'GFG_USER_4'],

                  index=['Practice1', 'Practice2', 'Practice3'])

print(df, "\n")

# Filter data using query method
df1 = df.loc[df.query(
    'GFG_USER_1 <= 80 & GFG_USER_2 > 10 & \
    GFG_USER_3 < 50 &  GFG_USER_4 == 80').index]

print(df1)
```

**输出:**

![](img/3debc7586513957efe771d8a49dd6f32.png)

**例**T2【2:

## 蟒蛇 3

```py
import pandas as pd

df = pd.DataFrame([[100, 200, 300], [70, 140, 210], 
                   [55, 150, 180]],

                  columns=['PAK', 'AUS', 'IND'],

                  index=['Match1', 'Match2', 'Match3'])

print(df, "\n")

# Filter data using query method
df1 = df.loc[df.query('PAK <= 80 & AUS > 100 & IND < 250').index]

print(df1)
```

**输出:**

![](img/1d689abc82ff55fb64b9596b0ab4b91b.png)

**例 3:**

## 蟒蛇 3

```py
import pandas as pd

df = pd.DataFrame([[1000, 2000, 3000, 4000], [7000, 1400, 2100, 2800], 
                   [5500, 1500, 800, 1200]],

                  columns=['DSA_Self_Paced', 'OOPS', 'DBMS', 'System_design'],

                  index=['Sale1', 'Sale2', 'Sale3'])

print(df, "\n")

# Filter data using query method
df1 = df.loc[df.query(
    'DSA_Self_Paced <= 6000 & OOPS > 1400 & DBMS < 1500 \
    &  System_design == 1200').index]

print(df1)
```

**输出:**

![](img/fc813de81935c6a0ef985e7e886beb5b.png)
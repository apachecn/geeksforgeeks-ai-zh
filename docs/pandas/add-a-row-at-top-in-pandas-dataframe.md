# 在熊猫数据框顶部增加一行

> 原文:[https://www . geesforgeks . org/add-a-row-top-in-pandas-data frame/](https://www.geeksforgeeks.org/add-a-row-at-top-in-pandas-dataframe/)

[Pandas DataFrame](https://www.geeksforgeeks.org/python-pandas-dataframe/) 是一个二维可变大小、潜在异构的表格数据结构，带有标记轴(行和列)。
让我们看看如何在熊猫数据框的顶部添加一行。
先观察这个数据集。

## 蟒蛇 3

```
# importing pandas module
import pandas as pd

# making data frame
df = pd.read_csv("https://media.geeksforgeeks.org/wp-content/uploads/nba.csv")

df.head(10)
```

![](img/226e9e8f64806663ac99a6ec9423a6c6.png)

**代码#1:** 通过连接旧数据帧和新数据帧，在给定数据帧的顶部添加行。

## 蟒蛇 3

```
new_row = pd.DataFrame({'Name':'Geeks', 'Team':'Boston', 'Number':3,
                        'Position':'PG', 'Age':33, 'Height':'6-2',
                        'Weight':189, 'College':'MIT', 'Salary':99999},
                                                            index =[0])
# simply concatenate both dataframes
df = pd.concat([new_row, df]).reset_index(drop = True)
df.head(5)
```

**输出:**

![](img/e157fb9e29dedc739c7b24cba62de604.png)

**代码#2:** 通过连接旧数据帧和新数据帧，在给定数据帧的顶部添加行。

## 蟒蛇 3

```
new_row = pd.DataFrame({'Name':'Geeks', 'Team':'Boston', 'Number':3,
                        'Position':'PG', 'Age':33, 'Height':'6-2',
                        'Weight':189, 'College':'MIT', 'Salary':99999}, index =[0])

# Concatenate new_row with df
df = pd.concat([new_row, df[:]]).reset_index(drop = True)
df.head(5)
```

**输出:**

![](img/e157fb9e29dedc739c7b24cba62de604.png)

**代码#3:** 通过使用 df.ix[]方法将旧数据框与新数据框连接起来，在给定数据框的顶部添加行。

## 蟒蛇 3

```
new_row = pd.DataFrame({'Name':'Geeks', 'Team':'Boston', 'Number':3,
                        'Position':'PG', 'Age':33, 'Height':'6-2',
                        'Weight':189, 'College':'MIT', 'Salary':99999}, index =[0])

df = pd.concat([new_row, df.ix[:]]).reset_index(drop = True)
df.head(5)
```

**输出:**

![](img/e157fb9e29dedc739c7b24cba62de604.png)
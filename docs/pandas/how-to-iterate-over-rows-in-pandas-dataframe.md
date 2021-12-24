# 如何迭代熊猫数据框中的行

> 原文:[https://www . geesforgeks . org/如何迭代熊猫中的行-dataframe/](https://www.geeksforgeeks.org/how-to-iterate-over-rows-in-pandas-dataframe/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 Python 包的奇妙生态系统。 ***【熊猫】*** 就是其中一个包，让导入和分析数据变得容易多了。

让我们看看如何使用`inerrows()`和`itertuples()`迭代熊猫数据框中的行:

**方法#1:** 使用`DataFrame.iterrows()`方法

该方法以(索引、序列)对的形式遍历行。

```
# importing pandas
import pandas as pd

# list of dicts
input_df = [{'name':'Sujeet', 'age':10},
            {'name':'Sameer', 'age':11},
            {'name':'Sumit', 'age':12}]

df = pd.DataFrame(input_df)
print('Original DataFrame: \n', df)

print('\nRows iterated using iterrows() : ')
for index, row in df.iterrows():
    print(row['name'], row['age'])
```

**Output:**

```
Original DataFrame: 
    age    name
0   10  Sujeet
1   11  Sameer
2   12   Sumit

Rows iterated using iterrows() : 
Sujeet 10
Sameer 11
Sumit 12

```

**方法 2:** 使用`DataFrame.itertuples()`方法

此方法为每一行返回一个命名元组。`getattr()`函数可以用来获取返回元组中的`row` 属性。这个方法比方法#1 更快。

```
# importing pandas
import pandas as pd

# list of dicts
input_df = [{'name':'Sujeet', 'age':10},
            {'name':'Sameer', 'age':110},
            {'name':'Sumit', 'age':120}]

df = pd.DataFrame(input_df)
print('Original DataFrame: \n', df)

print('\nRows iterated using itertuples() : ')
for row in df.itertuples():
    print(getattr(row, 'name'), getattr(row, 'age'))
```

**Output:**

```
Original DataFrame: 
    age    name
0   10  Sujeet
1  110  Sameer
2  120   Sumit

Rows iterated using itertuples() : 
Sujeet 10
Sameer 110
Sumit 120

```

我们很少有其他方法可以迭代熊猫数据框中的行。参见[在熊猫数据框](https://www.geeksforgeeks.org/different-ways-to-iterate-over-rows-in-pandas-dataframe/)中迭代行的不同方法。
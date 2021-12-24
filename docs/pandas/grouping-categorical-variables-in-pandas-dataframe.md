# 将熊猫数据框中的分类变量分组

> 原文:[https://www . geesforgeks . org/group-classic-变量-in-pandas-dataframe/](https://www.geeksforgeeks.org/grouping-categorical-variables-in-pandas-dataframe/)

首先，我们必须了解熊猫的分类变量是什么。范畴是 python 熊猫库中可用的数据类型。分类变量只接受固定类别(通常是固定数量)的值。分类变量的一些例子有性别、血型、语言等。与这些变量的一个主要对比是，这些变量不能执行任何数学运算。

可以使用**数据框**构造函数并指定**数据类型=“类别”**，在熊猫中创建由分类值组成的数据框。

## 蟒 3

```
# importing pandas as pd 
import pandas as pd 

# Create the dataframe 
# with categorical variable 
df = pd.DataFrame({'A': ['a', 'b', 'c',
                         'c', 'a', 'b'],
                   'B': [0, 1, 1, 0, 1, 0]},
                  dtype = "category")
# show the data types
df.dtypes
```
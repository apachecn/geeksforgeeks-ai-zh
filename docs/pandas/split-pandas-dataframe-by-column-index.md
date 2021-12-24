# 按列索引分割熊猫数据帧

> 原文:[https://www . geesforgeks . org/split-pandas-data frame-by-column-index/](https://www.geeksforgeeks.org/split-pandas-dataframe-by-column-index/)

Pandas 支持两种数据结构来存储数据:序列(单列)和数据帧，其中值存储在 2D 表(行和列)中。要使用索引对数据帧进行索引，我们需要使用 [dataframe.iloc()](https://www.geeksforgeeks.org/python-extracting-rows-using-pandas-iloc/) 方法，该方法需要

> ***句法:**熊猫。DataFrame.iloc[]*
> 
> ***参数:***
> ***索引位置:**整数或整数列表中行的索引位置。*
> 
> ***返回类型:**数据框或系列取决于参数*

让我们创建一个数据帧。在下面的例子中，我们将使用一个简单的二元数据集来分类一个物种是哺乳动物还是爬行动物。物种栏包含标签，其中 1 代表哺乳动物，0 代表爬行动物。数据存储在字典中，字典可以传递给输出数据帧的数据帧函数。

## 蟒蛇 3

```py
import pandas as pd

dataset = {'toothed': [1, 1, 1, 0, 1, 1, 1, 1, 1, 0],
           'hair': [1, 1, 0, 1, 1, 1, 0, 0, 1, 0],
           'breathes': [1, 1, 1, 1, 1, 1, 0, 1, 1, 1],
           'legs': [1, 1, 0, 1, 1, 1, 0, 0, 1, 1],
           'species': [1, 1, 0, 1, 1, 1, 0, 0, 1, 0]
           }

df = pd.DataFrame(dataset)

df.head()
```
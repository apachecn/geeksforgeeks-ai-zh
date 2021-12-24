# 蟒蛇|熊猫。分类()

> 原文:[https://www.geeksforgeeks.org/python-pandas-categorical/](https://www.geeksforgeeks.org/python-pandas-categorical/)

**熊猫。分类(值，类别=无，有序=无，数据类型=无):**它代表一个分类变量。范畴是熊猫的数据类型，对应于统计学中的范畴变量。这样的变量具有固定且有限数量的可能值。例如，等级、性别、血型等。
同样，在分类变量的情况下，逻辑顺序与分类数据不同，例如“一”、“二”、“三”。但是这些变量的排序使用逻辑顺序。

```
***Parameters-*** val        : [list-like] The values of categorical. 
categories : [index like] Unique categorisation of the categories. 
ordered    : [boolean] If false, then the categorical is treated as unordered. 
dtype      : [CategoricalDtype] an instance. 

***Error-*** ValueError :  If the categories do not validate. 
TypeError  :  If an explicit ordered = True but categorical can't be sorted. 

Return- Categorical variable
```

**代码:**

## 蟒蛇 3

```
# Python code explaining
# numpy.pandas.Categorical()

# importing libraries
import numpy as np
import pandas as pd

# Categorical using dtype
c = pd.Series(["a", "b", "d", "a", "d"], dtype ="category")
print ("\nCategorical without pandas.Categorical() : \n", c)

c1 = pd.Categorical([1, 2, 3, 1, 2, 3])
print ("\n\nc1 : ", c1)

c2 = pd.Categorical(['e', 'm', 'f', 'i',
                     'f', 'e', 'h', 'm' ])
print ("\nc2 : ", c2)
```
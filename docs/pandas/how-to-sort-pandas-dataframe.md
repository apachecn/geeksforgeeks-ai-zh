# 熊猫数据帧如何排序？

> 原文:[https://www.geeksforgeeks.org/how-to-sort-pandas-dataframe/](https://www.geeksforgeeks.org/how-to-sort-pandas-dataframe/)

在本文中，我们将讨论如何对熊猫数据帧进行排序。让我们创建一个数据帧。

**例:**

## 蟒 3

```py
# importing pandas library
import pandas as pd

# creating and initializing a nested list
age_list = [['Afghanistan', 1952, 8425333, 'Asia'],
            ['Australia', 1957, 9712569, 'Oceania'],
            ['Brazil', 1962, 76039390, 'Americas'],
            ['China', 1957, 637408000, 'Asia'],
            ['France', 1957, 44310863, 'Europe'],
            ['India', 1952, 3.72e+08, 'Asia'],
            ['United States', 1957, 171984000, 'Americas']]

# creating a pandas dataframe
df = pd.DataFrame(age_list, columns=['Country', 'Year',
                                     'Population', 'Continent'])

df
```
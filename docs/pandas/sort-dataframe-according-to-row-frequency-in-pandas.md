# 根据熊猫中的行频率对数据帧进行排序

> 原文:[https://www . geeksforgeeks . org/sort-data frame-按行-频率-in-pandas/](https://www.geeksforgeeks.org/sort-dataframe-according-to-row-frequency-in-pandas/)

在本文中，我们将讨论如何在熊猫中使用 [count()](https://www.geeksforgeeks.org/python-pandas-dataframe-count/) 和 [sort_values()](https://www.geeksforgeeks.org/python-pandas-dataframe-sort_values-set-1/) 。所以 pandas 中的计数计算数据帧列中元素的频率，然后根据元素频率对数据帧进行排序。

*   **count ():** This method will display the numerical value of each column in the data frame.
*   **sort _ values ():** This method helps us sort data frames. In this method, we pass the column, and our data frame is sorted according to the column.

**例 1:** 根据元素频率对数据帧进行降序排序的程序。

## 蟒蛇

```
# import pandas
import pandas as pd

# create dataframe
df = pd.DataFrame({'Name': ['Mukul', 'Rohan', 'Mukul', 'Manoj',
                            'Kamal', 'Rohan', 'Robin'],

                   'age': [22, 22, 21, 20, 21, 24, 20]})

# print dataframe
print(df)

# use count() and sort()
df = df.groupby(['Name'])['age'].count().reset_index(
  name='Count').sort_values(['Count'], ascending=False)

# print dataframe
print(df)
```
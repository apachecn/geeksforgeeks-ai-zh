# 在熊猫数据框的一列中用零替换所有的 NaN 值

> 原文:[https://www . geeksforgeeks . org/将所有 nan 值替换为熊猫数据框列中的零/](https://www.geeksforgeeks.org/replace-all-the-nan-values-with-zeros-in-a-column-of-a-pandas-dataframe/)

使用一行 **DataFrame.fillna()** 和 **DataFrame.replace()** 方法可以很容易地替换数据帧中的 NaN 或空值。我们将讨论这些方法以及一个演示如何使用它的例子。

## DataFrame.fillna():

此方法用于用特定值填充空值。

> **语法:** DataFrame.fillna(自身，值=无，方法=无，轴=无，位置=假，限制=无，向下转换=无)
> 
> **参数:**该方法将采用以下参数:
> 
> *   **值(标量、字典、序列或数据帧):**指定用于填充空值的值。
> *   **方法(['回填'，'填充'，'填充'，'填充'，'无'，默认无):**指定用于填充空值的方法。
> *   **轴(0 或“索引”，1 或“列”):**指定填充缺失值的轴。
> *   **就地(布尔值，默认为假):**如果布尔值为真，则就地填充，这将修改此对象上的任何其他视图。
> *   **限制(int，默认无):**指定向前/向后填充的连续 NaN 值的最大数量。
> *   **向下转换(dict，默认值为无):**如果可能的话，向下转换的项目数据类型的 dict，或者尝试向下转换为适当的相等类型(例如，如果可能的话，从 float64 到 int64)的字符串“expert”。
> 
> **返回:**数据帧或无。填充了空值的对象，如果 inplace=True，则为无。

**代码:**创建数据框。

## 蟒蛇 3

```py
# Import Pandas Library
import pandas as pd

# Import Numpy Library
import numpy as np

# Create a DataFrame
df = pd.DataFrame([[np.nan, 2, 3, np.nan],
                   [3, 4, np.nan, 1],
                   [1, np.nan, np.nan, 5],
                   [np.nan, 3, np.nan, 4]])

# Show the DataFrame
print(df)
```

**输出:**

![dataframe with NaN values](img/8f44af94c5214eee16f2d6fb07155401.png)

**代码:**用零替换所有的 NaN 值

## 蟒蛇 3

```py
# Filling null values
# with 0
df.fillna(value = 0,
          inplace = True)

# Show the DataFrame
print(df)
```
# 计算熊猫数据框的列数

> 原文:[https://www . geesforgeks . org/count-熊猫的列数-dataframe/](https://www.geeksforgeeks.org/count-number-of-columns-of-a-pandas-dataframe/)

我们来讨论一下如何计算[熊猫数据帧的列数。](https://www.geeksforgeeks.org/python-pandas-dataframe/)首先制作一个数据帧。

**例:**

## 蟒 3

```py
# Import Required Libraries
import pandas as pd
import numpy as np

# Create a dictionary for the dataframe
dict = {'Name': ['Sukritin', 'Sumit Tyagi', 'Akriti Goel',
                 'Sanskriti', 'Abhishek Jain'], 
        'Age': [22, 20, np.inf, -np.inf, 22], 
        'Marks': [90, 84, 33, 87, 82]}

# Converting Dictionary to Pandas Dataframe
df = pd.DataFrame(dict)

# Print Dataframe
df
```
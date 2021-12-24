# 从给定熊猫数据框中删除无限值

> 原文:[https://www . geesforgeks . org/remove-给定熊猫的无限值-dataframe/](https://www.geeksforgeeks.org/remove-infinite-values-from-a-given-pandas-dataframe/)

让我们讨论如何从[熊猫数据框](https://www.geeksforgeeks.org/python-pandas-dataframe/)中移除无限值。首先，让我们制作一个数据帧:

**例:**

## 蟒 3

```
# Import Required Libraries
import pandas as pd
import numpy as np

# Create a dictionary for the dataframe
dict = {'Name': ['Sumit Tyagi', 'Sukritin', 'Akriti Goel',
                 'Sanskriti', 'Abhishek Jain'],
        'Age': [22, 20, np.inf, -np.inf, 22], 
        'Marks': [90, 84, 33, 87, 82]}

# Converting Dictionary to Pandas Dataframe
df = pd.DataFrame(dict)

# Print Dataframe
df
```
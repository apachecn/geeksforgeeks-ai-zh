# 熊猫-蟒蛇中一列的对数和自然对数值

> 原文:[https://www . geesforgeks . org/log-and-natural-对数值-熊猫-python/](https://www.geeksforgeeks.org/log-and-natural-logarithmic-value-of-a-column-in-pandas-python/)

熊猫中一列的对数和自然对数值可以分别使用**[**log()**](https://www.geeksforgeeks.org/numpy-log-python/)[**log 2()**](https://www.geeksforgeeks.org/numpy-log2-python/)和**[**log 10()**](https://www.geeksforgeeks.org/numpy-log10-python/)**numpy 函数计算。在应用函数之前，我们需要创建一个数据帧。******

********代号:********

 ****## 蟒 3

```
# Import required libraries
import pandas as pd
import numpy as np

# Dictionary
data = {
     'Name': ['Geek1', 'Geek2',
             'Geek3', 'Geek4'],
   'Salary': [18000, 20000, 
             15000, 35000]} 

# Create a dataframe
data = pd.DataFrame(data,
                    columns = ['Name', 
                               'Salary'])

# Show the dataframe
data
```****
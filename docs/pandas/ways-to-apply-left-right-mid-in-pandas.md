# 熊猫应用左、右、中的方法

> 原文:[https://www . geesforgeks . org/申请方式-左-右-熊猫中部/](https://www.geeksforgeeks.org/ways-to-apply-left-right-mid-in-pandas/)

很多时候，我们需要提取熊猫数据框中字符串中的特定字符。为了解决这个问题，我们在熊猫中有左、右、中的概念。

**示例 1:** 从左侧提取字符

## python 3

```
# importing pandas library
import pandas as pd

# creating and initializing a list 
Cars = ['1000-BMW','2000-Audi','3000-Volkswagen',
        '4000-Datsun','5000-Toyota','6000-Maruti Suzuki']

# creating a pandas dataframe
df = pd.DataFrame(Cars, columns= ['Model_name'])

# Extracting characters from right side
# using slicing and storing result in 
# 'Left'
Left = df['Model_name'].str[:4]

print(Left)
```
# 将λ函数应用于熊猫数据帧

> 原文:[https://www . geeksforgeeks . org/application-lambda-functions-to-pandas-data frame/](https://www.geeksforgeeks.org/applying-lambda-functions-to-pandas-dataframe/)

在 Pandas 中，我们可以根据需要随时添加不同的函数，比如 lambda 函数、sort 函数等。我们可以将 lambda 函数应用于 Pandas 数据框的列和行。

**示例 1:** 使用 data frame . assign()

## python 3

将**λ**函数应用于**单列**

```
# importing pandas library
import pandas as pd

# creating and initializing a list
values= [['Rohan',455],['Elvish',250],['Deepak',495],
         ['Soni',400],['Radhika',350],['Vansh',450]] 

# creating a pandas dataframe
df = pd.DataFrame(values,columns=['Name','Total_Marks'])

# Applying lambda function to find 
# percentage of 'Total_Marks' column 
# using df.assign()
df = df.assign(Percentage = lambda x: (x['Total_Marks'] /500 * 100))

# displaying the data frame
df
```
# 如何将熊猫数据框列转换为系列？

> 原文:[https://www . geesforgeks . org/如何转换-pandas-data frame-columns-to-a-series/](https://www.geeksforgeeks.org/how-to-convert-pandas-dataframe-columns-to-a-series/)

在 pandas 中，可以将 pandas 数据框的列转换为序列。有时需要将数据框的列转换为另一种类型，如用于分析数据集的系列。

**情况 1:** 将数据框的**第一列**转换为**系列**

## python 3

```
# Importing pandas module
import pandas as pd

# Creating a dictionary 
dit = {'August': [10, 25, 34, 4.85, 71.2, 1.1], 
       'September': [4.8, 54, 68, 9.25, 58, 0.9], 
       'October': [78, 5.8, 8.52, 12, 1.6, 11], 
       'November': [100, 5.8, 50, 8.9, 77, 10] }

# Converting it to data frame
df = pd.DataFrame(data=dit)

# Original DataFrame
df
```
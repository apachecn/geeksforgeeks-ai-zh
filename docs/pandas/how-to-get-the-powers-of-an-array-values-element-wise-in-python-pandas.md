# 如何在 Python-Pandas 中逐元素获取数组值的幂？

> 原文:[https://www . geeksforgeeks . org/如何获取数组的幂值-python 中的元素-pandas/](https://www.geeksforgeeks.org/how-to-get-the-powers-of-an-array-values-element-wise-in-python-pandas/)

让我们看看如何按元素获取数组值的幂。[**data frame/Series . pow()**](https://www.geeksforgeeks.org/python-pandas-series-pow/)用于计算元素的幂，可以是自身的幂，也可以是其他系列的幂。这个函数只适用于实数，不会给出复数的结果。
让我们来看看节目:

**示例 1:** 一维数组被映射到一个 pandas 系列，该系列具有默认的数字索引或自定义索引，然后相应的元素被提升到它自己的幂。

## 蟒蛇 3

```
# import required modules
import numpy as np
import pandas as pd 

# create an array
sample_array = np.array([1, 2, 3])  

# uni dimensional arrays can be
# mapped to pandas series
sr = pd.Series(sample_array) 

print ("Original Array :")
print (sr)

# calculating element-wise power 
power_array = sr.pow(sr)

print ("Element-wise power array")
print (power_array)
```
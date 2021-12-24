# Python | Pandas series . str . isspace()方法

> 原文:[https://www . geesforgeks . org/python-pandas-series-str-isspace-method/](https://www.geeksforgeeks.org/python-pandas-series-str-isspace-method/)

Python 是进行数据分析的优秀语言，主要是因为以数据为中心的 Python 包的奇妙生态系统。熊猫就是其中之一，它让数据的导入和分析变得更加容易。

熊猫 **`isspace()`** 是一个字符串方法，它检查一个序列中的全空格字符，并且只为那些元素返回真。由于它是一个字符串方法， ***字符串*** 必须在每次调用这个方法之前加上前缀。

> **语法:**Series . str . isspace()
> T3】返回类型:布尔系列

**示例#1:**
在此示例中，使用 Pandas 从 python 列表中制作了一个系列。Series()方法。默认情况下，该序列是一个字符串序列，其中一些元素为全空格。对序列调用`str.isspace()`方法，结果存储在变量 result1 中并显示。

```
# importing pandas module  
import pandas as pd  

# importing numpy module 
import numpy as np 

# creating series 1 
series1 = pd.Series(['a', 'b', '  ', ' c ', 'd', '  ', np.nan]) 

# checking for all space elements in series1
result1 = series1.str.isspace()

# display
print('Series 1 results:\n\n', result1)
```

**输出:**
如输出所示，对应元素为 All-space 的地方返回 True，否则返回 False。同样可以看出，序列中的最后一个元素是`np.nan`，因此输出也是 NaN。

```
Series 1 results:

 0    False
1    False
2     True
3    False
4    False
5     True
6      NaN
dtype: object
```

**示例 2:** 使用`.astype()`处理错误和转换序列

因为这是一个仅适用于字符串系列的字符串方法。将其应用于数值序列会返回值错误。因此，该系列的数据类型必须转换为 str，这样该方法才能工作。使用熊猫`astype()`转换系列的数据类型。

```
# importing pandas module  
import pandas as pd  

# creating series 2 
series2 = pd.Series([1, 2, 3, 10, 2]) 

# try except for series2
# since series 2 is a numeric series
try:
    result2 = series2.str.isspace()
    print('Series 2 results: \n\n', result2)

except Exception as e:

    # printing error in
    print('\nError occured - {}'.format(e))

    # new result by first converting to string series
    # using .astype()
    result2 = series2.astype(str).str.isspace()

    # printing results
    print('\nSeries 2 results: \n\n', result2)
```

**输出:**
可以看到，对数值序列调用这个方法会返回一个值错误。数据需要使用。astype()方法。因为所有的值都是数字，而不是全空格，所以所有的值都返回 False。

```
Error occured - Can only use .str accessor with string values, 
which use np.object_ dtype in pandas

Series 2 results: 

 0    False
1    False
2    False
3    False
4    False
dtype: bool
```
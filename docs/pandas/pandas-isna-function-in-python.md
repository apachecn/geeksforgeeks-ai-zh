# pandas.isna()函数在 Python 中

> 原文:[https://www . geesforgeks . org/pandas-ISNA-function-in-python/](https://www.geeksforgeeks.org/pandas-isna-function-in-python/)

此方法用于检测类似数组的对象的缺失值。该函数接受标量或类似数组的对象，并指示值是否缺失(数值数组中的“NaN”，对象数组中的“None”或“NaN”，datetimelike 中的“NaT”)。

> **语法:** pandas.isna(obj)
> 
> **参数:**
> 
> *   **对象:**标量或类似数组的对象，用于检查空值或缺失值。

下面是上述方法的实现，并附有一些例子:

**例 1 :**

## 蟒蛇 3

```
# importing package
import numpy
import pandas

# string "deep" is not nan value
print(pandas.isna("deep"))

# numpy.nan represents a nan value
print(pandas.isna(numpy.nan))
```

**输出:**

```
False
True

```

**例 2 :**

## 蟒蛇 3

```
# importing package
import numpy
import pandas

# create and view data
array = numpy.array([[1, numpy.nan, 3], 
                     [4, 5, numpy.nan]])

print(array)

# numpy.nan represents a nan value
print(pandas.isna(array))
```

**输出:**

```
[[ 1\. nan  3.]
 [ 4\.  5\. nan]]
[[False  True False]
 [False False  True]]

```
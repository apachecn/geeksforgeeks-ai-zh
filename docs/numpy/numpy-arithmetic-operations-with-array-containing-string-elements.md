# NumPy–包含字符串元素的数组的算术运算

> 原文:[https://www . geeksforgeeks . org/numpy-包含字符串元素的数组算术运算/](https://www.geeksforgeeks.org/numpy-arithmetic-operations-with-array-containing-string-elements/)

Numpy 是一个 Python 库，用于用 C 和 Python 编写的数组处理。numpy 中的计算比 Python 中的传统数据结构(如列表、元组、字典等)快得多。由于矢量化的通用函数。有时在处理数据时，我们需要执行算术运算，但由于数据中存在不需要的字符串，我们无法这样做。因此有必要将它们移除。在这里，我们将创建一个通用函数，将不需要的字符串替换为 NaN。

**解释:**
给定一个包含一些不想要的字符串的 numpy 数组。在用户定义的函数中，使用条件语句将不需要的字符串替换为 NaN。 *numpy.frompyfunc()* 用于将用户自定义函数转换为通用函数。numpy 数组然后被传递给该函数，但是数组的数据类型仍然是一个对象。因此，我们需要使用 *array.astype()* 将其数据类型转换为 float。应该注意的是，NaN 值不能转换为除浮点以外的任何其他数据类型。现在，我们可以使用内置通用函数的 NaN 安全版本对其执行算术运算。

**代码:**

```py
# Importing numpy library
import numpy as gfg

# Creating array
a = gfg.array([1,2,3,'geeks','for','geeks',4,5])
print(f"Actual array: {a}")

# Creating universal function to remove unwanted 
# strings from actual array
def m(a):
    if a == 'geeks'or a=='for':
        return gfg.nan
    else:
        return float(a)

# Converting user-defined function to universal function  
b = gfg.frompyfunc(m,1,1)

# Calling function
a = b(a)

# Changing datatype of array
a = a.astype(float)
print(f"Array after changes: {a}")

# Calculating mean of the array
m = gfg.nanmean(a)
print(f"Mean of the array: {m}")

# Calculating sum of the array
s = gfg.nansum(a)
print(f"Sum of the array: {s}")

# Calculating product of the array
p = gfg.nanprod(a)
print(f"Product of the array: {p}")
```

**输出:**

```py
Actual array: ['1' '2' '3' 'geeks' 'for' 'geeks' '4' '5']
Array after changes: [ 1\.  2\.  3\. nan nan nan  4\.  5.]
Mean of the array: 3.0
Sum of the array: 15.0
Product of the array: 120.0
```
# 如何用空格分割给定 NumPy 数组的元素？

> 原文:[https://www . geeksforgeeks . org/如何用空格分割给定 numpy 数组的元素/](https://www.geeksforgeeks.org/how-to-split-the-element-of-a-given-numpy-array-with-spaces/)

要用空格分割给定数组的元素，我们将使用 [numpy.char.split()](https://www.geeksforgeeks.org/numpy-string-operations-split-function/) 。这是一个在 NumPy 中进行字符串操作的函数。它返回字符串中的单词列表，使用 sep 作为 arr 中每个元素的分隔符字符串。

> ***参数:***
> ***arr :** 类似字符串或 unicode 的数组。输入数组。*
> ***sep :** 【字符串或 unicode，可选】指定拆分字符串时使用的分隔符。*
> ***最大劈叉:**要做多少个最大劈叉。*
> 
> ***返回:**【非数组】包含列表对象的输出数组。*

**例 1:**

## 蟒蛇 3

```py
import numpy as np

# Original Array
array = np.array(['PHP C# Python C Java C++'], dtype=np.str)
print(array)

# Split the element of the said array with spaces
sparr = np.char.split(array)
print(sparr)
```
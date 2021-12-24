# Python 中 NumPy 数组如何转换成字典？

> 原文:[https://www . geesforgeks . org/how-convert-numpy-array-to-dictionary-in-python/](https://www.geeksforgeeks.org/how-to-convert-numpy-array-to-dictionary-in-python/)

下面的文章解释了如何在 Python 中将 [numpy 数组](https://www.geeksforgeeks.org/python-numpy/)转换为[字典](https://www.geeksforgeeks.org/python-dictionary/)。Numpy 中的 Array 是一个元素表(通常是数字)，所有元素都是相同的类型，由一组正整数索引。在 Numpy 中，数组的维数称为数组的秩。 给出数组沿每个维度的大小的整数元组称为数组的形状。Numpy 中的数组类称为 **数组** 。Numpy 数组中的元素通过使用方括号来访问，并且可以通过使用嵌套的 Python 列表来初始化。

### 方法

要将 numpy 数组转换为字典，以下程序使用***dict(enumerate(array . flat()，1))*** 这正是它的作用:

*   ***array.flat** : This function is used to get a copy of a given array and fold it into one dimension.*
**   [**Enumeration**](https://www.geeksforgeeks.org/enumerate-in-python/) : The enumeration method provides an automatic counter/index for each item in the list. The first index value will start at 0.*   [**dict**](https://www.geeksforgeeks.org/python-dictionary/) : This function is used to convert any object into a dictionary.*

***例 1:***

 *## 蟒 3

```py
# importing required librariess
import numpy as np

# creating a numpy array
array = np.array([['a', 'b', 'c'],
                  ['d', 'e', 'f'],
                  ['g', 'h', 'i']])

# convert numpy array to dictionary
d = dict(enumerate(array.flatten(), 1))

# print numpy array
print(array)
print(type(array))

# print dictionary
print(d)
print(type(d))
```*
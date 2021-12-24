# 如何将 NumPy 数组转换为列表？

> 原文:[https://www . geesforgeks . org/how-convert-numpy-array-to-list/](https://www.geeksforgeeks.org/how-to-convert-numpy-array-to-list/)

在本文中，我们将讨论如何将 NumPy 数组转换为列表。我们可以通过 **tolist()** 方法将 Numpy 数组转换为列表，我们可以有一个数据元素列表，该列表是使用该方法从数组转换而来的。

> **语法:***ndarray . tolist()*
> 
> ***参数:**无*
> 
> ***返回:**可能嵌套的数组元素列表。*

### 方法

*   导入所需模块。
*   创建数组。
*   显示数组和类类型。
*   使用 **tolist()** 方法转换数组。
*   显示列表和类别类型。

**例 1:** 一维阵

## 蟒

```
# import module
import numpy as np

# create array
print("\nArray:")
arr = np.array([1, 2, 4, 5])  
print(arr)
print(type(arr))

# apply method
lis = arr.tolist()

# display list
print("\nList:")
print(lis)
print(type(lis))
```
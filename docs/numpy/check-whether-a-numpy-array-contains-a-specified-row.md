# 检查 Numpy 数组是否包含指定的行

> 原文:[https://www . geesforgeks . org/check-a-numpy-array-contains-a-specified-row/](https://www.geeksforgeeks.org/check-whether-a-numpy-array-contains-a-specified-row/)

在本文中，我们将了解检查指定行是否在 [NumPy 数组](https://www.geeksforgeeks.org/python-numpy/#:~:text=Array%20in%20Numpy%20is%20a,a%20tuple%20of%20positive%20integers.&text=An%20array%20class%20in%20Numpy,by%20using%20nested%20Python%20Lists.)中。如果给定列表在 NumPy 数组中以行的形式出现，则输出为真，否则为假。列表出现在 numpy 数组中意味着该 NumPy 数组中的任何一行都与给定列表匹配，所有元素都按给定顺序排列。这可以通过使用简单的方法来完成，例如用给定的列表检查每一行，但是这可以通过使用内置的库函数[来容易地理解和实现。](https://www.geeksforgeeks.org/python-numpy-ndarray-tolist/)

> *语法 ndar . tolist()*
> 
> ***参数:**无*
> 
> ***返回:**数组元素的可能嵌套列表。*

**示例:**

> Arr = [[1，2，3，4，5]，[6，7，8，9，10]，[11，12，13，14，15]，[16，17，18，19，20]]
> 
> 给定的列表如下:
> 
> lst = [1，2，3，4，5] **True** ，因为它与第 0 行匹配。
> 【16，17，20，19，18】**假**，因为和任何一排都不匹配。
> 【3，2，5，-4，5】**假**，因为和任何一行都不匹配。
> 【11，12，13，14，15】**为真**，与第 2 行匹配。

下面是一个示例的实现:

## 蟒蛇 3

```
# importing package
import numpy

# create numpy array
arr = numpy.array([[1, 2, 3, 4, 5],
                   [6, 7, 8, 9, 10],
                   [11, 12, 13, 14, 15],
                   [16, 17, 18, 19, 20]
                   ])

# view array
print(arr)

# check for some lists
print([1, 2, 3, 4, 5] in arr.tolist())
print([16, 17, 20, 19, 18] in arr.tolist())
print([3, 2, 5, -4, 5] in arr.tolist())
print([11, 12, 13, 14, 15] in arr.tolist())
```

**输出:**

```
[[ 1  2  3  4  5]
 [ 6  7  8  9 10]
 [11 12 13 14 15]
 [16 17 18 19 20]]
True
False
False
True

```
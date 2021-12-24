# 如何将一个列表和元组转换成 NumPy 数组？

> 原文:[https://www . geeksforgeeks . org/如何将列表和元组转换为 numpy 数组/](https://www.geeksforgeeks.org/how-to-convert-a-list-and-tuple-into-numpy-arrays/)

在本文中，让我们讨论如何使用 NumPy 将列表和元组转换为数组。NumPy 提供了各种方法来做到这一点。让我们讨论一下

**方法 1:** 使用[纽姆帕瑞()](https://www.geeksforgeeks.org/numpy-asarray-in-python/)

它将输入转换为数组。输入可以是元组的列表、元组、元组的元组、列表的元组和数组。

**语法:**

```py
numpy.asarray(  a, type = None, order = None ) 
```

**示例:**

## 蟒蛇 3

```py
import numpy as np

# list
list1 = [3, 4, 5, 6]
print(type(list1))
print(list1)
print()

# conversion
array1 = np.asarray(list1)
print(type(array1))
print(array1)
print()

# tuple
tuple1 = ([8, 4, 6], [1, 2, 3])
print(type(tuple1))
print(tuple1)
print()

# conversion
array2 = np.asarray(tuple1)
print(type(array2))
print(array2)
```

**输出:**

```py
<class 'list'>
[3, 4, 5, 6]

<class 'numpy.ndarray'>
[3 4 5 6]

<class 'tuple'>
([8, 4, 6], [1, 2, 3])

<class 'numpy.ndarray'>
[[8 4 6]
 [1 2 3]]

```

**方法 2:** 使用 numpy.array()

它创建一个数组。

> **语法:** numpy.array(对象，dtype = None，* copy = True，order = 'K '，subok = False，ndmin = 0)
> 
> **参数:**
> 
> 1.  **物体:**阵列状
> 2.  **数据类型:**数据类型，可选(数组所需的数据类型。如果没有给出，那么类型将被确定为保持序列中的对象所需的最小类型。)
> 3.  **复制:** bool，可选(如果为真(默认)，则复制对象。否则，只有当 __array__ 返回一个副本，如果 obj 是一个嵌套序列，或者需要一个副本来满足任何其他要求(数据类型、顺序等)时，才会创建一个副本。).)
> 4.  **顺序:** {'K '，' A '，' C '，' F'}，可选(同上)
> 5.  **subok:** bool，可选(如果为 True，则传递子类，否则返回的数组将被强制为基类数组(默认)。)
> 6.  **ndmin:** int，可选(指定结果数组应具有的最小维数。其中一个将根据需要预先悬挂在形状上，以满足这一要求。)
> 
> **返回:**n 数组(满足指定要求的数组对象。)

**示例:**

## 蟒蛇 3

```py
import numpy as np

# list
list1 = [1, 2, 3]
print(type(list1))
print(list1)
print()

# conversion
array1 = np.array(list1)
print(type(array1))
print(array1)
print()

# tuple
tuple1 = ((1, 2, 3))
print(type(tuple1))
print(tuple1)
print()

# conversion
array2 = np.array(tuple1)
print(type(array2))
print(array2)
print()

# list, array and tuple
array3 = np.array([tuple1, list1, array2])
print(type(array3))
print(array3)
```

**输出:**

```py
<class 'list'>
[1, 2, 3]

<class 'numpy.ndarray'>
[1 2 3]

<class 'tuple'>
(1, 2, 3)

<class 'numpy.ndarray'>
[1 2 3]

<class 'numpy.ndarray'>
[[1 2 3]
 [1 2 3]
 [1 2 3]]
```
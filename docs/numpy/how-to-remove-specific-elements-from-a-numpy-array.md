# 如何从 NumPy 数组中移除特定元素？

> 原文:[https://www . geeksforgeeks . org/如何从 numpy 数组中移除特定元素/](https://www.geeksforgeeks.org/how-to-remove-specific-elements-from-a-numpy-array/)

在本文中，我们将讨论如何从 NumPy 数组中移除特定元素。将使用 **delete()** 方法进行同样的操作。

**语法:**

> numpy.delete(数组名，索引值)
> 
> 其中 array_name 是要删除的数组的名称，index-value 是要删除的元素的索引。

例如，我们有一个包含 5 个元素的数组，

```
array1=[1,2,3,4,5]
```

索引从 0 到 n-1 开始。如果我们要删除 2，那么 2 元素索引就是 1。所以，我们可以指定

```
np.delete(array1,1)
```

如果我们想一次删除多个元素，即 1，2，3，4，5，您可以指定列表中的所有索引元素。

```
np.delete(array1,[0,1,2,3,4])
```

下面是一些我们移除 NumPy 数组中特定元素的例子。

**例 1:**

程序创建一个包含 5 个元素的数组并删除第一个元素。

## 蟒蛇 3

```
# import numpy as np
import numpy as np

# create an array with 5 elements
a = np.array([1, 2, 3, 4, 5])

# display a
print(a)

# delete 1 st element
print("remaining elements after deleting 1st element ",
      np.delete(a, 0))
```
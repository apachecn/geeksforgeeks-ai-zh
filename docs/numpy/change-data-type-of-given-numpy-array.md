# 改变给定 numpy 数组的数据类型

> 原文:[https://www . geesforgeks . org/change-data-type-of-给定-numpy-array/](https://www.geeksforgeeks.org/change-data-type-of-given-numpy-array/)

在这篇文章中，我们将看到改变给定 numpy 数组的数据类型的方法。为了改变给定数组对象的数据类型，我们将使用`numpy.astype()`函数。该函数接受一个作为目标数据类型的参数。该函数支持所有数据的泛型类型和内置类型。

**问题#1 :** 给定一个 numpy 数组，其底层数据为`'int32'`类型。将给定对象的数据类型更改为`'float64'`。

**解决方案:**我们将使用`numpy.astype()`函数来更改给定 numpy 数组的底层数据的数据类型。

```
# importing the numpy library as np
import numpy as np

# Create a numpy array
arr = np.array([10, 20, 30, 40, 50])

# Print the array
print(arr)
```

**输出:**

![](img/9d6a172dbe62eae48d129c4e7982cf4a.png)

现在我们将检查给定数组对象的数据类型。

```
# Print the dtype
print(arr.dtype)
```

**输出:**

![](img/cd63f151081374fd1247b0f93a59d91e.png)

正如我们在输出中看到的，给定数组对象的当前数据类型是“int32”。现在我们将把它改为“float64”型。

```
# change the dtype to 'float64'
arr = arr.astype('float64')

# Print the array after changing
# the data type
print(arr)

# Also print the data type
print(arr.dtype)
```

**输出:**

![](img/135c654414830f7c93d007ad703f4712.png)

![](img/8b7cedce262233b3071bf656ea465162.png)

**问题 2 :** 给定一个 numpy 数组，其底层数据为`'int32'`类型。将给定对象的数据类型更改为`'complex128'`。

**解决方案:**我们将使用`numpy.astype()`函数来更改给定 numpy 数组的底层数据的数据类型。

```
# importing the numpy library as np
import numpy as np

# Create a numpy array
arr = np.array([10, 20, 30, 40, 50])

# Print the array
print(arr)
```

**输出:**

![](img/9d6a172dbe62eae48d129c4e7982cf4a.png)

现在我们将检查给定数组对象的数据类型。

```
# Print the dtype
print(arr.dtype)
```

**输出:**

![](img/cd63f151081374fd1247b0f93a59d91e.png)

正如我们在输出中看到的，给定数组对象的当前数据类型是“int32”。现在我们将把它改为“complex128”类型。

```
# change the dtype to 'complex128'
arr = arr = arr.astype('complex128')

# Print the array after changing
# the data type
print(arr)

# Also print the data type
print(arr.dtype)
```

**输出:**

![](img/ede9be432a11803d2b9b397f7bcb1cfd.png)

![](img/32992e79a7f03bfc4a4e430d24cb1a0b.png)
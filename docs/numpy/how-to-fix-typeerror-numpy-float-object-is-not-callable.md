# 如何修复:type error:“numpy . float”对象不可调用？

> 原文:[https://www . geesforgeks . org/how-fix-type error-numpy-float-object-不可调用/](https://www.geeksforgeeks.org/how-to-fix-typeerror-numpy-float-object-is-not-callable/)

在本文中，我们将看到如何修复类型错误:“numpy.float”对象在 Python 中不可调用。只有一种情况下我们可以看到这个错误:

如果我们试图调用一个 NumPy 数组作为函数，我们最有可能得到这样的错误。

**示例:**

## 蟒蛇 3

```py
import numpy as np

a = np.array([1,2,3])

a()
```

**输出:**

```py
TypeError: 'numpy.ndarray' object is not callable
```

在旧版本的 Numpy 中，我们以前看到的是“numpy.float64”，而不是“numpy.ndarray”。

**解决方案:**

这可以简单地通过删除数组后面的括号来解决。

## 蟒 3

```py
import numpy as np

a = np.array([1,2,3])

a
```

**输出:**

```py
array([1, 2, 3])
```

这里的 NumPy 版本是‘1 . 21 . 2’。

**注**:在早期版本的 NumPy 中，我们也曾经在使用 Python min()或 max()函数搭配 Numpy 数组的时候得到这个错误。在 NumPy 的最新版本中，这个问题得到了解决。在早期版本中，应该使用 np.max()或 np.min()而不是 min()和 max()来解决此特定错误。
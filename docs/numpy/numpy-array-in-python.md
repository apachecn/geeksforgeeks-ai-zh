# Python 中的 NumPy 数组

> 原文:[https://www.geeksforgeeks.org/numpy-array-in-python/](https://www.geeksforgeeks.org/numpy-array-in-python/)

Python 列表是数组的替代品，但是它们无法在计算大量数值数据时提供所需的性能。为了解决这个问题，我们使用了一个名为 NumPy 的 python 库。NumPy 这个词代表数字 Python。NumPy 提供了一个名为[的数组对象。它们类似于标准 python 序列，但在某些关键因素上有所不同。](https://www.geeksforgeeks.org/numpy-ndarray/)

## **NumPy 数组与内置 Python 序列的对比**

*   与列表不同，NumPy 数组的大小是固定的，更改数组的大小将导致创建一个新数组，而原始数组将被删除。
*   数组中的所有元素都是同一类型的。
*   Numpy 数组比标准 python 序列更快、更高效，并且需要更少的语法。

**注意:**各种基于科学数学 Python 的包都使用 Numpy。他们可能会将输入作为一个内置的 Python 序列，但他们可能会将数据转换为 NumPy 数组，以便获得更快的处理速度。这就解释了理解 NumPy 的必要性。

## **为什么 Numpy 这么快？**

Numpy 数组大部分是用 C 语言编写的。由于是用 C 语言编写的，NumPy 数组存储在连续的内存位置，这使得它们易于访问和操作。这意味着您可以轻松编写 python 程序，从而获得 C 代码的性能水平。

### **使用 Numpy 阵列**

如果您的系统中没有安装 NumPy，您可以按照以下步骤进行操作。安装 NumPy 后，您可以像这样将其导入程序中

```py
import numpy as np

```

这里 np 是 NumPy 常用的别名。

### **列表中的 Numpy 数组**

您可以使用 np 别名使用 array()方法创建列表的数组。

```py
li = [1,2,3,4]
numpyArr = np.array(li)

```

或者

```py
numpyArr = np.array([1,2,3,4])

```

该列表被传递给 array()方法，然后该方法返回一个具有相同元素的 NumPy 数组。

**示例:**

下面的示例显示了如何从列表中初始化 NumPy 数组。

## 蟒 3

```py
import numpy as np

li = [1, 2, 3, 4]
numpyArr = np.array(li)
print(numpyArr)
```
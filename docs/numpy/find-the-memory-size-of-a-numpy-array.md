# 找出 NumPy 数组的内存大小

> 原文:[https://www . geesforgeks . org/find-内存大小的 numpy-array/](https://www.geeksforgeeks.org/find-the-memory-size-of-a-numpy-array/)

在这篇文章中，我们将看到如何找到 NumPy 数组的内存大小。因此，为了找到内存大小，我们使用以下方法:

**方法 1:** 使用**大小**和**项目化**NumPy 数组的属性。

> **大小:**该属性给出了 NumPy 数组中存在的元素数量。
> 
> **itemsize:** 该属性给出了 NumPy 数组中一个元素的内存大小，单位为字节。

让我们看看例子:

**例 1:**

## 蟒蛇 3

```py
# import library
import numpy as np

# create a numpy 1d-array
x = np.array([100,20,34])

print("Size of the array: ",
      x.size)

print("Memory size of one array element in bytes: ",
      x.itemsize)

# memory size of numpy array in bytes
print("Memory size of numpy array in bytes:",
      x.size * x.itemsize)
```

**输出:**

```py
Size of the array:  3
Memory size of one array element in bytes:  4
Memory size of numpy array in bytes: 12

```

**例 2:**

## 蟒蛇 3

```py
# import library
import numpy as np

# create a numpy 2d-array
x = np.array([[100, 20, 34],
              [300, 400, 600]])

print("Size of the array: ",
      x.size)

print("Memory size of one array element in bytes: ",
      x.itemsize)

# memory size of numpy array
print("Memory size of numpy array in bytes:",
      x.size * x.itemsize)
```

**输出:**

```py
Size of the array:  6
Length of one array element in bytes:  4
Memory size of numpy array in bytes: 24

```

**方法二:**利用 NumPy 数组的 **nbytes** 属性。

> **nbytes:** 该属性给出了 NumPy 数组元素消耗的总字节数。

让我们看看例子:

**例 1:**

## 蟒蛇 3

```py
# import library
import numpy as np

# create numpy 1d-array
x = np.array([100, 20, 34])

print("Memory size of a NumPy array:",
      x.nbytes)
```

**输出:**

```py
Memory size of a NumPy array: 12

```

**例 2:**

## 蟒蛇 3

```py
# import library
import numpy as np

# create numpy 2d-array
x = np.array([[100, 20, 34],
              [300, 400, 600]])

print("Memory size of a NumPy array:",
      x.nbytes)
```

**输出:**

```py
Memory size of a NumPy array: 24

```
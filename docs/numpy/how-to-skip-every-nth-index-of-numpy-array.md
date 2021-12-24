# 如何跳过 NumPy 数组的每第 n 个索引？

> 原文:[https://www . geeksforgeeks . org/如何跳过每 n 个数组索引/](https://www.geeksforgeeks.org/how-to-skip-every-nth-index-of-numpy-array/)

在本文中，我们将看到如何跳过 NumPy 数组的每第 n 个索引。有多种方法可以访问和跳过 NumPy 数组的元素:

**方法 1:天真方法**

可以维护一个计数器来记录到目前为止遍历的元素的计数，然后一旦遇到第 N 个位置，就跳过该元素，并将计数器重置为 0。除了遍历时遇到的第 n 个索引元素，所有元素都被追加到一个新列表中。在此期间所需的时间相当于 O(n)，其中 n 是 numpy 数组的大小。如果元素只需要打印而不需要存储，我们可以跳过创建另一个数组的声明。

**示例:**

## 蟒蛇 3

```py
# importing required packages
import numpy as np

# declaring a numpy array
x = np.array([1.2, 3.0, 6.7, 8.7, 8.2,
              1.3, 4.5, 6.5, 1.2, 3.0,
              6.7, 8.7, 8.2, 1.3, 4.5, 
              6.5])

# skipping every 4th element
n = 4

# declaring new list
new_arr = []

# maintaining cntr
cntr = 0

# looping over array
for i in x:

    # checking if element is nth pos
    if(cntr % n != 0):
        new_arr.append(i)

    # incrementing counter
    cntr += 1

print("Array after skipping nth element")
print(new_arr)
```

**输出:**

> 跳过第 n 个元素后的数组
> 
> [3.0, 6.7, 8.7, 1.3, 4.5, 6.5, 3.0, 6.7, 8.7, 1.3, 4.5, 6.5]

**方法二:采用 NumPy 模量法**

首先可以使用 [numpy.arange()](https://www.geeksforgeeks.org/numpy-arange-python/) 方法将数组排列成均匀间隔的块。

> **语法:**名词短语(开始、停止、步骤)
> 
> **参数:**
> 
> *   **开始:**间隔的开始
> *   **停止:**间隔结束
> *   **步骤:**开始和结束间隔之间的步骤

然后， [np.mod()](https://www.geeksforgeeks.org/numpy-mod-in-python/) 方法应用于获得的列表区间，然后用第 n 个索引计算每个元素的模。原始数组中模输出不为 0 的元素作为最终列表返回。

**例**

## 蟒蛇 3

```py
# importing required packages
import numpy as np

# declaring a numpy array
x = np.array([0, 1, 2, 3, 2, 5, 2, 7, 2, 9])

print("Original Array")
print(x)

# skipping third element
new_arr = x[np.mod(np.arange(x.size), 3) != 0]

print("Array after skipping elements : ")
print(new_arr)
```

**输出:**

> 原始数组
> 
> [0 1 2 3 2 5 2 7 2 9]
> 
> 跳过元素后的数组:
> 
> [1 2 2 5 7 2]

**方法三:NumPy 切片**

NumPy 切片基本上是数据二次采样，我们在其中创建原始数据的视图，这会产生恒定的时间。对原始数组进行更改，并将整个原始数组保存在内存中。也可以显式制作数据的副本。

**语法:**

> arr[开始:结束:st]

这里，开始是起始索引，结束是停止索引，st 是步长，步长不等于 0。并且，它返回一个包含分别属于 st 索引的元素的子数组。假设数组的索引从 0 开始。

**例**

## 计算机编程语言

```py
# importing required packages
import numpy as np

# declaring a numpy array
x = np.array([0, 1, 2, 3, 2, 5, 2, 7, 2, 9])

# calculating length of array
length = len(x)

# accessing every third element 
# from the array
print("List after n=3rd element access")
print(x[0:length:3])
```

**输出:**

> n=第三次元素访问后的列表
> 
> [0 3 2 9]
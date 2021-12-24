# 找出一个序列在 NumPy 数组中出现的次数

> 原文:[https://www . geeksforgeeks . org/find-numpy 数组中序列的出现次数/](https://www.geeksforgeeks.org/find-the-number-of-occurrences-of-a-sequence-in-a-numpy-array/)

该序列由列表形式的一些元素组成，我们必须找到该序列在给定 NumPy 数组中出现的次数。这可以通过检查 ndarray 每次迭代的序列来轻松完成。但是这会导致更长的时间，所以我们使用 NumPy 方法的概念。

**例:**

```py
Arr = [[2,8,9,4],
       [9,4,9,4],
       [4,5,9,7],
       [2,9,4,3]]
and the seq = [9,4] then output is 4.

Here, 
first row [2,8,9,4] 
contains one [9,4] sequence so output = 1.

second row [9,4,9,4] 
contains two [9,4] sequence so output = 1+2 = 3.

third row [4,5,9,7] 
contains no [9,4] sequence so output = 3+0 = 3.

fourth row [2,9,4,3] 
contains one [9,4] sequence so output = 3+1 = 4.
```

下面是用一个例子来实现:

## python 3

```py
# importing package
import numpy

# create numpy array
arr = numpy.array([[2, 8, 9, 4], 
                   [9, 4, 9, 4],
                   [4, 5, 9, 7],
                   [2, 9, 4, 3]])

# Counting sequence
output = repr(arr).count("9, 4")

# view output
print(output)
```

**输出:**

```py
4

```
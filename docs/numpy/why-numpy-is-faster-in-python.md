# 为什么 Python 中的 Numpy 更快？

> 原文:[https://www . geeksforgeeks . org/why-numpy-is-fast-in-python/](https://www.geeksforgeeks.org/why-numpy-is-faster-in-python/)

NumPy 是一个 Python 基础包，用于对高级数学函数、多维数组、线性代数、傅立叶变换、随机数功能等进行高效的操作和运算。它提供了在 Python 中集成 C、C++和 Fortran 代码的工具。NumPy 在 Python 中主要用于科学计算。

让我们看看下面的程序，它从执行时间的角度比较了 Python 中的 NumPy 数组和列表。

## 蟒蛇 3

```
# importing required packages
import numpy
import time

# size of arrays and lists
size = 1000000  

# declaring lists
list1 = range(size)
list2 = range(size)

# declaring arrays
array1 = numpy.arange(size) 
array2 = numpy.arange(size)

# list
initialTime = time.time()
resultantList = [(a * b) for a, b in zip(list1, list2)]

# calculating execution time
print("Time taken by Lists :",
      (time.time() - initialTime),
      "seconds")

# NumPy array
initialTime = time.time()
resultantArray = array1 * array2

# calculating execution time
print("Time taken by NumPy Arrays :",
      (time.time() - initialTime),
      "seconds")
```

**输出:**

```
Time taken by Lists : 1.1984527111053467 seconds
Time taken by NumPy Arrays : 0.13434123992919922 seconds
```

从上面程序的输出中，我们看到 NumPy 数组的执行速度比 Python 中的 Lists 快得多。数组和列表的执行时间差别很大。

**NumPy 数组比 Python Lists 快，原因如下:**

*   数组是存储在连续内存位置的同类数据类型的集合。另一方面，Python 中的列表是存储在非连续内存位置的异构数据类型的集合。
*   NumPy 包将一个任务分解成多个片段，然后并行处理所有的片段。
*   NumPy 包集成了 Python 中的 C、C++和 Fortran 代码。与 Python 相比，这些编程语言的执行时间非常少。

下面是一个比较 NumPy 数组和 Python Lists 上不同操作执行时间的程序:

## 蟒蛇 3

```
# importing required packages
import numpy
import time

# size of arrays and lists
size = 1000000 

# declaring lists
list1 = [i for i in range(size)]
list2 = [i for i in range(size)]

# declaring arrays
array1 = numpy.arange(size)
array2 = numpy.arange(size)

# Concatenation
print("\nConcatenation:")

# list
initialTime = time.time()
list1 = list1 + list2

# calculating execution time
print("Time taken by Lists :",
      (time.time() - initialTime),
      "seconds")

# NumPy array
initialTime = time.time()
array = numpy.concatenate((array1, array2),
                          axis = 0)

# calculating execution time
print("Time taken by NumPy Arrays :",
      (time.time() - initialTime),
      "seconds")

# Dot Product
dot = 0
print("\nDot Product:")

# list
initialTime = time.time()
for a, b in zip(list1, list2):
        dot = dot + (a * b)

# calculating execution time
print("Time taken by Lists :",
      (time.time() - initialTime),
      "seconds")

# NumPy array
initialTime = time.time()
array = numpy.dot(array1, array2)

# calculating execution time
print("Time taken by NumPy Arrays :",
      (time.time() - initialTime),
      "seconds")

# Scalar Addition
print("\nScalar Addition:")

# list
initialTime = time.time()
list1 =[i + 2 for i in range(size)]

# calculating execution time
print("Time taken by Lists :",
      (time.time() - initialTime),
      "seconds")

# NumPy array
initialTime = time.time()
array1 = array1 + 2

# calculating execution time
print("Time taken by NumPy Arrays :",
      (time.time() - initialTime),
      "seconds")

# Deletion
print("\nDeletion: ")

# list
initialTime = time.time()
del(list1)

# calculating execution time
print("Time taken by Lists :",
      (time.time() - initialTime),
      "seconds")

# NumPy array
initialTime = time.time()
del(array1)

# calculating execution time
print("Time taken by NumPy Arrays :",
      (time.time() - initialTime),
      "seconds")
```

**输出:**

```
Concatenation:
Time taken by Lists : 0.02946329116821289 seconds
Time taken by NumPy Arrays : 0.011709213256835938 seconds

Dot Product:
Time taken by Lists : 0.179551362991333 seconds
Time taken by NumPy Arrays : 0.004144191741943359 seconds

Scalar Addition:
Time taken by Lists : 0.09385180473327637 seconds
Time taken by NumPy Arrays : 0.005884408950805664 seconds

Deletion: 
Time taken by Lists : 0.01268625259399414 seconds
Time taken by NumPy Arrays : 3.814697265625e-06 seconds
```

从上面的程序中，我们得出结论，对 NumPy 数组的操作比 Python 列表执行得更快。此外，与程序中的其他操作相比，删除操作在数组和列表之间的执行时间差异最大。
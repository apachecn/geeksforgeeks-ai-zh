# Python 列表 VS Numpy 数组

> 原文:[https://www.geeksforgeeks.org/python-lists-vs-numpy-arrays/](https://www.geeksforgeeks.org/python-lists-vs-numpy-arrays/)

**NumPy** 是 Python 中科学计算的基础包。 [NumPy](https://www.geeksforgeeks.org/python-numpy/) 阵列便于对大量数据进行高级数学和其他类型的运算。通常，与使用 Python 的内置序列相比，这样的操作执行效率更高，代码更少。NumPy 不是另一种编程语言，而是 Python 扩展模块。它在同构数据阵列上提供快速高效的操作。

**关于 Numpy 数组的一些要点:**

*   我们可以使用 numpy.array()在 python 中创建一个 N 维数组。
*   默认情况下，数组是同构的，这意味着数组中的数据必须是相同的数据类型。(注意也可以用 python 创建结构化数组)。
*   元素级操作是可能的。
*   Numpy 数组有各种各样的函数、方法和变量，以简化我们的矩阵计算任务。
*   数组的元素连续存储在内存中。例如，二维数组的所有行必须具有相同的列数。或者一个三维数组在每张卡片上必须有相同的行数和列数。

**Numpy 数组的表示:**

*   一维数字阵列；

    ```py
    import numpy as np

    a = np.array([1, 2, 3])
    print(a)
    ```

    **输出:**

    ```py
    [1 2 3]

    ```

*   多维 Numpy 数组:

    ```py
    import numpy as np

    a = np.array([(1, 2, 3), (4, 5, 6)])
    print(a)
    ```

    **输出:**

    ```py
    [[1 2 3]
     [4 5 6]]

    ```

**使用 Numpy 数组优于 Python 列表的优势:**

*   消耗更少的内存。
*   与 python 列表相比速度更快。
*   使用方便。

**列表:** A [列表](https://www.geeksforgeeks.org/python-list/)是一个有序可变的集合。在 Python 中，列表是用方括号写的。

**关于 Python 列表的一些要点:**

*   列表可以是同类的，也可以是异类的。
*   列表上不可能有元素操作。
*   Python 列表默认为一维。但是我们可以创建一个多维列表。但这也将是一个存储另一个 1 D 名单的一维列表
*   列表的元素不需要在内存中连续。

下面是一些例子，通过分析内存消耗、执行时间比较和两者支持的操作，清楚地展示了 Numpy 数组如何优于 Python 列表。

**示例 1:Numpy 数组和列表之间的内存消耗**
在本例中，将创建一个 Python 列表和一个大小为 1000 的 Numpy 数组。将计算每个元素的大小，然后计算两个容器的整体大小，并根据内存消耗进行比较。

下面是实现。

```py
# importing numpy package
import numpy as np

# importing system module
import sys

# declaring a list of 1000 elements 
S= range(1000)

# printing size of each element of the list
print("Size of each element of list in bytes: ",sys.getsizeof(S))

# printing size of the whole list
print("Size of the whole list in bytes: ",sys.getsizeof(S)*len(S))

# declaring a Numpy array of 1000 elements 
D= np.arange(1000)

# printing size of each element of the Numpy array
print("Size of each element of the Numpy array in bytes: ",D.itemsize)

# printing size of the whole Numpy array
print("Size of the whole Numpy array in bytes: ",D.size*D.itemsize)
```

**Output:**

```py
Size of each element of list in bytes:  48
Size of the whole list in bytes:  48000
Size of each element of the Numpy array in bytes:  8
Size of the whole Numpy array in bytes:  8000

```

**示例 2:Numpy 数组和 Python 列表的时间比较**
在本例中，将创建 2 个 Python 列表和 2 个 Numpy 数组，每个容器有 1000000 个元素。将分别对列表和 Numpy 数组中的元素进行乘法运算，并分析两个容器执行所需的时间差异，以确定哪一个执行该操作花费的时间更少。

下面是实现。

```py
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

# capturing time before the multiplication of Python lists
initialTime = time.time()

# multiplying  elements of both the lists and stored in another list
resultantList = [(a * b) for a, b in zip(list1, list2)]

# calculating execution time
print("Time taken by Lists to perform multiplication:", 
      (time.time() - initialTime),
      "seconds")

# capturing time before the multiplication of Numpy arrays
initialTime = time.time()

# multiplying  elements of both the Numpy arrays and stored in another Numpy array 
resultantArray = array1 * array2

# calculating execution time 
print("Time taken by NumPy Arrays to perform multiplication:",
      (time.time() - initialTime),
      "seconds")
```

**Output:**

```py
Time taken by Lists : 0.15030384063720703 seconds
Time taken by NumPy Arrays : 0.005921125411987305 seconds

```

**示例 3:操作对 Numpy 数组和 Python 列表的影响**
在此示例中，演示了 Python 列表无法执行基本操作。将声明一个 Python 列表和一个具有相同元素的 Numpy 数组，并添加一个整数，以该整数值递增容器的每个元素，而不循环语句。将分析此操作对 Numpy 数组和 Python 列表的影响。

下面是实现。

```py
# importing Numpy package
import numpy as np

# declaring a list
ls =[1, 2, 3]

# converting the list into a Numpy array
arr = np.array(ls)

try:
    # adding 4 to each element of list
    ls = ls + 4

except(TypeError):
    print("Lists don't support list + int")

# now on array
try:
    # adding 4 to each element of Numpy array
    arr = arr + 4

    # printing the Numpy array
    print("Modified Numpy array: ",arr)

except(TypeError):
    print("Numpy arrays don't support list + int")
```

**Output:**

```py
Lists don't support list + int
Modified Numpy array: [5 6 7]

```
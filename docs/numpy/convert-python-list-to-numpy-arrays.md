# 将 Python 列表转换为 numpy 数组

> 原文:[https://www . geesforgeks . org/convert-python-list-to-numpy-arrays/](https://www.geeksforgeeks.org/convert-python-list-to-numpy-arrays/)

Python 中的[列表](https://www.geeksforgeeks.org/python-list/)是一种线性数据结构，可以保存不需要声明的异构元素，并且可以灵活收缩和增长。另一方面，数组是一种可以保存同构元素的数据结构，数组是使用 [NumPy](https://www.geeksforgeeks.org/python-numpy/) 库在 Python 中实现的。数组比列表需要更少的内存。

数组和列表的相似之处在于，数组和列表的元素都可以通过其索引值来识别。
**在 Python 中列表可以通过使用 NumPy 库中的两种方法转换为数组:**

*   **使用 numpy.array()**

## 蟒蛇 3

```py
# importing library
import numpy

# initializing list
lst = [1, 7, 0, 6, 2, 5, 6]

# converting list to array
arr = numpy.array(lst)

# displaying list
print ("List: ", lst)

# displaying array
print ("Array: ", arr)
```

**输出:**

```py
List:  [1, 7, 0, 6, 2, 5, 6]
Array:  [1 7 0 6 2 5 6]
```

*   **使用 numpy.asarray()**

## 蟒蛇 3

```py
# importing library
import numpy

# initializing list
lst = [1, 7, 0, 6, 2, 5, 6]

# converting list to array
arr = numpy.asarray(lst)

# displaying list
print ("List:", lst)

# displaying array
print ("Array: ", arr)
```

**输出:**

```py
List:  [1, 7, 0, 6, 2, 5, 6]
Array:  [1 7 0 6 2 5 6]
```

以上两种方法的重要区别在于 numpy.array()将复制原始对象，numpy.asarray()将镜像原始对象中的更改。即:

当使用 numpy.asarray()创建数组副本时，一个数组中所做的更改也会反映在另一个数组中，但不会显示创建数组时所依据的列表中的更改。但是，numpy.array()不会出现这种情况。

## 蟒蛇 3

```py
# importing library
import numpy

# initializing list
lst = [1, 7, 0, 6, 2, 5, 6]

# converting list to array
arr = numpy.asarray(lst)

# displaying list
print ("List:", lst)

# displaying array
print ("arr: ", arr)

# made another array out of arr using asarray function
arr1 = numpy.asarray(arr)

#displaying arr1 before the changes made
print("arr1: " , arr1)

#change made in arr1
arr1[3] = 23

#displaying arr1 , arr , list after the change has been made
print("lst: " , lst)
print("arr: " , arr)
print("arr1: " , arr1)
```

**输出:**

```py
List: [1, 7, 0, 6, 2, 5, 6]
arr:  [1 7 0 6 2 5 6]
arr1:  [1 7 0 6 2 5 6]
lst:  [1, 7, 0, 6, 2, 5, 6]
arr:  [ 1  7  0 23  2  5  6]
arr1:  [ 1  7  0 23  2  5  6]
```

在“arr”和“arr1”中，变化在索引 3 处可见，但在索引 1 处不可见。
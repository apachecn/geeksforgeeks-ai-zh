# 找出 NumPy 数组中的最大和最小元素

> 原文:[https://www . geeksforgeeks . org/find-numpy 数组中的最大和最小元素/](https://www.geeksforgeeks.org/find-the-maximum-and-minimum-element-in-a-numpy-array/)

一个数组可以被认为是一个包含相同类型元素的容器。Python 将其数组模块命名为**数组**。我们可以简单地导入模块并创建我们的数组。但是这个模块有一些缺点。主要缺点是我们无法创建多维数组。并且数据类型必须相同。

为了克服这些问题，我们使用了名为 **NumPy** 的第三方模块。使用 NumPy，我们可以创建多维数组，也可以使用不同的数据类型。

**注意:默认情况下，NumPy** 不附带 python。所以，我们必须用 pip 安装它。要安装该模块，请在终端中运行给定的命令。

```py
pip install numpy
```

现在让我们使用 NumPy 创建一个数组。为此，我们需要导入模块。我们在这里导入模块。

```py
import numpy
```

使用上面的命令，您可以导入模块。

**示例 1:** 现在尝试创建一维数组。

```py
arr = numpy.array([1, 2, 3, 4, 5])
```

这里，我们创建一个一维整数 NumPy 数组。现在试着找到最大元素。为此，我们必须使用 **numpy.max(“数组名”)**函数。

**语法:**

```py
numpy.max(arr)
```

要找到最小元素，请使用 **numpy.min(“数组名”)**函数。

**语法:**

```py
numpy.min(arr)
```

**代码:**

## 蟒蛇 3

```py
# import numpy library
import numpy

# creating a numpy array of integers
arr = numpy.array([1, 5, 4, 8, 3, 7])

# finding the maximum and
# minimum element in the array
max_element = numpy.max(arr)
min_element = numpy.min(arr)

# printing the result
print('maximum element in the array is: ',
      max_element)
print('minimum element in the array is: ',
      min_element)
```

**输出:**

```py
maximum element in the array is:  8 
minimum element in the array is:  1
```

**注意:**必须使用数字(int 或 float)，不能使用字符串。

**示例 2:** 现在，让我们创建一个二维 NumPy 数组。

```py
arr = numpy.array([11, 5, 7],
        [4, 5, 16],
        [7, 81, 16]]
```

现在使用 **numpy.max()** 和 **numpy.min()** 函数，我们可以找到最大和最小元素。
这里，我们从整个数组中得到最大值和最小值。

**代码:**

## 蟒蛇 3

```py
# import numpy library
import numpy

# creating a two dimensional
# numpy array of integers
arr = numpy.array([[11, 2, 3],
                     [4, 5, 16],
                      [7, 81, 22]])

# finding the maximum and
# minimum element in the array
max_element = numpy.max(arr)
min_element = numpy.min(arr)

# printing the result
print('maximum element in the array is:',
      max_element)
print('minimum element in the array is:',
      min_element)
```

**输出:**

```py
maximum element in the array is: 81
minimum element in the array is: 2
```

**示例 3:** 现在，如果我们想要从行或列中找到最大值或最小值，那么我们必须添加 **0** 或 **1** 。看看它是如何工作的:

```py
maximum_element = numpy.max(arr, 0)
maximum_element = numpy.max(arr, 1)
```

如果我们使用 0，它会给出一个列表，其中包含每列的最大值或最小值。这里我们会得到一个像[11 81 22]这样的列表，每个列都有最大数量。

如果我们用 1 代替 0，将得到像[11 16 81]这样的列表，其中包含每行的最大数字。

**代码:**

## 蟒蛇 3

```py
# import numpy library
import numpy

# creating a two dimensional
# numpy array of integers
arr = numpy.array([[11, 2, 3],
                     [4, 5, 16],
                      [7, 81, 22]])

# finding the maximum and
# minimum element in the array
max_element_column = numpy.max(arr, 0)
max_element_row = numpy.max(arr, 1)

min_element_column = numpy.amin(arr, 0)
min_element_row = numpy.amin(arr, 1)

# printing the result
print('maximum elements in the columns of the array is:',
      max_element_column)

print('maximum elements in the rows of the array is:',
      max_element_row)

print('minimum elements in the columns of the array is:',
      min_element_column)

print('minimum elements in the rows of the array is:',
      min_element_row)
```

**输出:**

```py
maximum elements in the columns of the array is: [11 81 22]
maximum elements in the rows of the array is: [11 16 81]
minimum elements in the columns of the array is: [4 2 3]
minimum elements in the rows of the array is: [2 4 7]
```

**例 4:** 如果我们有两个形状相同的 NumPy 数组，我们可以找到最大或最小元素。对于这一步，我们需要 **numpy.maximum(array1，array2)** 函数。它将返回一个包含每列最大值的列表。

**代码:**

## 蟒蛇 3

```py
# importing numpy library
import numpy

# creating two single dimensional array
a = numpy.array([1, 4, 6, 8, 9])
b = numpy.array([5, 7, 3, 9, 22])

# print maximum value
print(numpy.maximum(a, b))
```

**输出:**

```py
[ 5  7  6  9 22]
```
# 使用 NumPy 在 Python 中索引多维数组

> 原文:[https://www . geesforgeks . org/indexing-多维-python 中的数组-使用-numpy/](https://www.geeksforgeeks.org/indexing-multi-dimensional-arrays-in-python-using-numpy/)

[NumPy](https://www.geeksforgeeks.org/python-numpy/) 是一个通用的数组处理包。它提供了一个高性能多维数组对象和使用这些数组的工具。它是使用 Python 进行科学计算的基本包。它包含各种功能。
**注:**更多信息请参考 [Python Numpy](http://geeksforgeeks.org/python-numpy/)
**示例:**

## 蟒蛇 3

```py
# numpy library imported
import numpy as np

# creating single-dimensional array
arr_s = np.arrange(5)
print(arr_s)
```

**输出:**

```py
[0 1 2 3 4]
```

**numpy 中的 array()**方法创建长度为 5 的一维数组。**排列()**方法中的单个参数充当范围的结束元素。**安排()**也采取开始和结束论点与步骤。
**例:**

## 蟒蛇 3

```py
import numpy as np

# here inside arrange method we
# provide start, end, step as
# arguments.
arr_b = np.arrange(20, 30, 2)

# step argument helps in printing
# every said step and skipping the
# rest.
print(arr_b)
```

**输出:**

```py
[20 22 24 26 28]
```

索引这些数组很简单。每个数组元素都有一个与之关联的特定索引。索引从 0 开始，一直到数组 1 的长度。在前面的例子中，arr_b 本身有 5 个元素。访问这些元素可以通过:
完成

```py
array_name[index_number]
```

**例:**

## 蟒蛇 3

```py
import numpy as np

# here inside arrange method we
# provide start, end, step as
# arguments.
arr_b = np.arrange(20, 30, 2)

# step argument helps in printing
# every said step and skipping the
# rest.
print(arr_b)

print(arr_b[2])

# Slicing operation from index
# 1 to 3
print(arr_b[1:4])
```

**输出**T2】

```py
[20 22 24 26 28]
24
[22 24 26]
```

对于**多维数组**可以使用**重塑()**方法和**排列()**

## 蟒蛇 3

```py
import numpy as np

arr_m = np.arrange(12).reshape(6, 2)
print(arr_m)
```

**输出:**

```py
[[ 0  1]
 [ 2  3]
 [ 4  5]
 [ 6  7]
 [ 8  9]
 [10 11]]
```

在**重塑()**内，参数应该是**排列()**参数的倍数。在前面的例子中，我们有 6 行 2 列。您可以指定另一个参数来定义数组的维度。默认情况下，它是二维数组。
**例:**

## 蟒蛇 3

```py
import numpy as np

arr_m = np.arrange(12).reshape(2, 2, 3)
print(arr_m)
```

**输出**T2】

```py
[[[ 0  1  2]
  [ 3  4  5]]

 [[ 6  7  8]
  [ 9 10 11]]]
```

要索引多维数组，可以使用类似于一维数组的切片操作进行索引。
**例:**

## 蟒蛇 3

```py
import numpy as np

arr_m = np.arrange(12).reshape(2, 2, 3)

# Indexing
print(arr_m[0:3])
print()
print(arr_m[1:5:2,::3])
```

**输出:**

```py
[[[ 0  1  2]
  [ 3  4  5]]

 [[ 6  7  8]
  [ 9 10 11]]]

[[[6 7 8]]]
```
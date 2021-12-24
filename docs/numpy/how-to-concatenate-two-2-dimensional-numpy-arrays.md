# 如何连接两个二维 NumPy 数组？

> 原文:[https://www . geeksforgeeks . org/如何连接二维 numpy 数组/](https://www.geeksforgeeks.org/how-to-concatenate-two-2-dimensional-numpy-arrays/)

有时，连接或合并两个或多个这些 [NumPy](https://www.geeksforgeeks.org/python-numpy/) 数组可能是有用的或必需的。在本文中，我们将讨论连接两个 2D 阵列的各种方法。但是首先，我们必须导入 NumPy 包才能使用它:

```
# import numpy package
import numpy as np
```

然后必须创建两个 2D 阵列来执行操作，通过使用 [**排列()**](https://www.geeksforgeeks.org/numpy-arange-python/) 和 [重塑()](https://www.geeksforgeeks.org/numpy-reshape-python/) 功能。使用 NumPy，我们可以以各种方式和方法执行多个 2D 阵列的拼接。

### **方法一:使用** **连接()** **功能**

我们可以使用 [**连接**](https://www.geeksforgeeks.org/numpy-concatenate-function-python/) **()** 功能来执行连接操作。使用这个函数，数组可以按行或按列连接，假设它们分别有相等的行或列。列级连接可以通过将轴等于 1 作为函数中的一个参数来实现。

**示例:**

## 计算机编程语言

```
# Program to concatenate two 2D arrays column-wise
# import numpy
import numpy as np

# Creating two 2D arrays
arr1 = np.arange(1,10).reshape(3,3)
arr2 = np.arange(10,19).reshape(3,3)
arr1
arr2

# Concatenating operation
# axis = 1 implies that it is being done column-wise
np.concatenate((arr1,arr2),axis=1)
```

**输出:**

```
array([[0, 1, 2],
       [3, 4, 5],
       [6, 7, 8]])

array([[10, 11, 12],
       [13, 14, 15],
       [16, 17, 18]])

array([[ 0,  1,  2, 10, 11, 12],
       [ 3,  4,  5, 13, 14, 15],
       [ 6,  7,  8, 16, 17, 18]])
```

同样，可以通过将轴等效为 0 来实现逐行串联。

**示例:**

## 计算机编程语言

```
# Program to concatenate two 2D arrays row-wise
import numpy as np

# Creating two 2D arrays
arr1 = np.arange(1, 10).reshape(3, 3)
arr2 = np.arange(10, 19).reshape(3, 3)

# Concatenating operation
# axis = 0 implies that it is being done row-wise
np.concatenate((arr1, arr2), axis=0)
```

**输出:**

```
array([[ 0,  1,  2],
       [ 3,  4,  5],
       [ 6,  7,  8],
       [10, 11, 12],
       [13, 14, 15],
       [16, 17, 18]])
```

### **方法二:使用** **叠加()** **功能:**

[堆叠()](https://www.geeksforgeeks.org/numpy-stack-in-python/)功能的使用方法与 **串联()** 功能相同，其中轴等于一。通过使用这个，阵列一个堆叠在另一个之上。

**示例:**

## 计算机编程语言

```
# Program to concatenate two 2D arrays row-wise
import numpy as np

arr1 = np.arange(1, 10).reshape(3, 3)
arr2 = np.arange(10, 19).reshape(3, 3)

# Concatenating operation
# axis = 1 implies that it is being
# done row-wise
np.stack((arr1, arr2), axis=1)
```

**输出:**

```
array([[[ 1,  2,  3],
        [10, 11, 12]],

       [[ 4,  5,  6],
        [13, 14, 15]],

       [[ 7,  8,  9],
        [16, 17, 18]]])
```

或者通过将轴等同于 2，连接与高度一起完成，如下所示。

**示例:**

## 蟒蛇 3

```
# Program to concatenate two 2D arrays along
# the height
import numpy as np

arr1 = np.arange(1, 10).reshape(3, 3)
arr2 = np.arange(10, 19).reshape(3, 3)

# Concatenating operation
# axis = 2 implies that it is being done
# along the height
np.stack((arr1, arr2), axis=2)
```

**输出:**

```
array([[[ 1, 10],
        [ 2, 11],
        [ 3, 12]],

       [[ 4, 13],
        [ 5, 14],
        [ 6, 15]],

       [[ 7, 16],
        [ 8, 17],
        [ 9, 18]]])
```

### **方法三:使用** **hstack()** **功能**

[](https://www.geeksforgeeks.org/numpy-hstack-in-python/)**函数将数组水平堆叠，即沿一列堆叠。**

****示例:****

## **计算机编程语言**

```
# Program to concatenate two 2D arrays
# horizontally
import numpy as np

arr1 = np.arange(1, 10).reshape(3, 3)
arr2 = np.arange(10, 19).reshape(3, 3)

# Concatenating operation
arr = np.hstack((arr1, arr2))
```

****输出:****

```
array([[ 0,  1,  2, 10, 11, 12],
       [ 3,  4,  5, 13, 14, 15],
       [ 6,  7,  8, 16, 17, 18]])
```

### ****方法四:使用** **vstack()** **功能****

**[**【vstack()**](https://www.geeksforgeeks.org/numpy-vstack-in-python/)函数垂直堆叠数组，即沿一行排列。**

****示例:****

## **计算机编程语言**

```
# Program to concatenate two 2D arrays
# vertically
import numpy as np

arr1 = np.arange(1, 10).reshape(3, 3)
arr2 = np.arange(10, 19).reshape(3, 3)

# Concatenating operation
arr = np.vstack((arr1, arr2))
```

****输出:****

```
array([[ 0,  1,  2],
       [ 3,  4,  5],
       [ 6,  7,  8],
       [10, 11, 12],
       [13, 14, 15],
       [16, 17, 18]])
```

### ****方法五:使用** **dstack()** **功能****

**在[**dstack(**](https://www.geeksforgeeks.org/python-numpy-dstack-method/)**)**功能中，d 代表深度，如下图所示，连接随高度一起出现:**

****示例:****

## **计算机编程语言**

```
# Program to concatenate two 2D arrays
# along the height
import numpy as np

arr1 = np.arange(1, 10).reshape(3, 3)
arr2 = np.arange(10, 19).reshape(3, 3)

# Concatenating operation
arr = np.dstack((arr1, arr2))
```

****输出:****

```
array([[[ 1, 10],
        [ 2, 11],
        [ 3, 12]],

       [[ 4, 13],
        [ 5, 14],
        [ 6, 15]],

       [[ 7, 16],
        [ 8, 17],
        [ 9, 18]]])
```

****方法 6** : **使用 column_stack()功能****

**column_stack()函数将数组水平堆叠，即沿着一列堆叠，它通常用于通过水平连接将 id 数组连接成 2d 数组。**

## **蟒蛇 3**

```
import numpy

array1 = numpy.array([[1, 2, 3, 4, 5],[20,30,40,50,60]])
array2 = numpy.array([[6, 7, 8, 9, 10],[9,8,7,6,5]])

# Stack arrays horizontally.
array1 = numpy.column_stack([array1, array2])
print(array1)
```

****输出:****

```
*[[ 1  2  3  4  5  6  7  8  9 10]*

 *[20 30 40 50 60  9  8  7  6  5]]*
```
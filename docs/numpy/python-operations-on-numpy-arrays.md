# Python:Numpy 数组上的操作

> 原文:[https://www . geeksforgeeks . org/python-operations-on-numpy-arrays/](https://www.geeksforgeeks.org/python-operations-on-numpy-arrays/)

[NumPy](https://www.geeksforgeeks.org/python-numpy/) 是 Python 包，意思是‘数值 Python’。它是逻辑计算的库，包含了强大的 n 维数组对象，给出了集成 C、C++等的工具。它同样有助于基于线性的数学、任意数字容量等。NumPy 展示同样可以用作通用数据的有效多维隔间。

**NumPy Array:** Numpy array 是一个强大的 N 维数组对象，以行和列的形式存在。我们可以从嵌套的 Python 列表中初始化 **NumPy 数组**并访问它的元素。结构层次上的 Numpy 数组由以下元素组合而成:

*   **数据**指针指示数组中第一个字节的内存地址。
*   **数据类型**或**数据类型**指针描述数组中包含的元素种类。
*   **形状**表示阵列的形状。
*   **步距**是内存中应该跳过的字节数，以便进入下一个元素。

#### Numpy 数组上的运算

**算术运算:**

```py
# Python code to perform arithmetic
# operations on NumPy array

import numpy as np 

# Initializing the array
arr1 = np.arange(4, dtype = np.float_).reshape(2, 2) 

print('First array:') 
print(arr1)

print('\nSecond array:') 
arr2 = np.array([12, 12]) 
print(arr2)

print('\nAdding the two arrays:') 
print(np.add(arr1, arr2))

print('\nSubtracting the two arrays:') 
print(np.subtract(arr1, arr2))

print('\nMultiplying the two arrays:')
print(np.multiply(arr1, arr2))

print('\nDividing the two arrays:')
print(np.divide(arr1, arr2))
```

**输出:**

```py
First array:
[[ 0\.  1.]
 [ 2\.  3.]]

Second array:
[12 12]

Adding the two arrays:
[[ 12\.  13.]
 [ 14\.  15.]]

Subtracting the two arrays:
[[-12\. -11.]
 [-10\.  -9.]]

Multiplying the two arrays:
[[  0\.  12.]
 [ 24\.  36.]]

Dividing the two arrays:
[[ 0\.          0.08333333]
 [ 0.16666667  0.25      ]]

```

**numpy.reciprocol（）**

这个函数按元素返回参数的倒数。对于绝对值大于 1 的元素，结果始终为 0，对于整数 0，将发出溢出警告。

**示例:**

```py
# Python code to perform reciprocal operation
# on NumPy array
import numpy as np 
arr = np.array([25, 1.33, 1, 1, 100]) 

print('Our array is:')
print(arr)

print('\nAfter applying reciprocal function:') 
print(np.reciprocal(arr))

arr2 = np.array([25], dtype = int)
print('\nThe second array is:')
print(arr2)

print('\nAfter applying reciprocal function:') 
print(np.reciprocal(arr2))
```

**输出**

```py
Our array is:
[  25\.      1.33    1\.      1\.    100\.  ]

After applying reciprocal function:
[ 0.04       0.7518797  1\.         1\.         0.01     ]

The second array is:
[25]

After applying reciprocal function:
[0]

```

num py . power()

此函数将第一个输入数组中的元素视为基数，并将其提升到第二个输入数组中相应元素的幂。

```py
# Python code to perform power operation
# on NumPy array

import numpy as np 

arr = np.array([5, 10, 15]) 

print('First array is:') 
print(arr)

print('\nApplying power function:') 
print(np.power(arr, 2))

print('\nSecond array is:') 
arr1 = np.array([1, 2, 3]) 
print(arr1)

print('\nApplying power function again:') 
print(np.power(arr, arr1))
```

**输出:**

```py
First array is:
[ 5 10 15]

Applying power function:
[ 25 100 225]

Second array is:
[1 2 3]

Applying power function again:
[   5  100 3375]

```

num py . mod()

该函数返回输入数组中相应元素的除法余数。函数`numpy.remainder()`也产生同样的结果。

```py
# Python code to perform mod function
# on NumPy array

import numpy as np 

arr = np.array([5, 15, 20]) 
arr1 = np.array([2, 5, 9]) 

print('First array:') 
print(arr) 

print('\nSecond array:') 
print(arr1)

print('\nApplying mod() function:') 
print(np.mod(arr, arr1))

print('\nApplying remainder() function:') 
print(np.remainder(arr, arr1))
```

**输出:**

```py
First array:
[ 5 15 20]

Second array:
[2 5 9]

Applying mod() function:
[1 0 2]

Applying remainder() function:
[1 0 2]

```
# 检查 NumPy

中的数据类型

> 原文:[https://www.geeksforgeeks.org/check-data-type-in-numpy/](https://www.geeksforgeeks.org/check-data-type-in-numpy/)

*Numpy* 是 python 中的一个模块。它最初被称为数字巨蟒，但简而言之，我们将其发音为 *numpy* 。 *NumPy* 是 python 中的通用数组处理包。它提供了高性能的多维数据结构，如数组对象和使用这些数组的工具。 *Numpy* 提供更快更有效的矩阵和数组计算。

*NumPy* 提供对几乎所有数学函数的熟悉。在 *numpy* 中，这些函数被称为通用函数 *ufunc* 。

### 以下是在 NumPy 中检查数据类型的各种值:

**方法#1**

使用*数据类型*检查数据类型。

**例 1:**

## 蟒 3

```
# importing numpy library
import numpy as np

# creating and initializing an array
arr = np.array([1, 2, 3, 23, 56, 100])

# printing the array and checking datatype
print('Array:', arr)

print('Datatype:', arr.dtype)
```

**输出:**

```
Array: [  1   2   3  23  56 100]
Datatype: int32
```

**例 2:**

## 蟒 3

```
import numpy as np

# creating and initializing array of string
arr_1 = np.array(['apple', 'ball', 'cat', 'dog'])

# printing array and its datatype
print('Array:', arr_1)

print('Datatype:', arr_1.dtype)
```

**输出:**

```
Array: ['a' 'b' 'c' 'd']
Datatype: <U1
```

**方法 2**

用定义的数据类型创建数组。使用数组函数*数组()*创建 *numpy* 数组。该函数采用参数*数据类型*，允许我们定义数组元素的预期数据类型:

**例 1:**

## 蟒 3

```
import numpy as np

# Creating and initializing array with datatype
arr = np.array([1, 2, 3, 8, 7, 5], dtype='S')

# printing array and its datatype
print("Array:", arr)
print("Datatype:", arr.dtype)
```

**输出:**

```
Array: [b'1' b'2' b'3' b'8' b'7' b'5']
Datatype: |S1
```

*S* 用于定义字符串数据类型。我们使用 *i、U、f、S* 和 *U* 来定义各种其他数据类型及其大小。

**例 2:**

## 蟒 3

```
import numpy as np

# creating and initialising array along
# with datatype and its size 4 i.e. 32bytes
arr = np.array([1, 2, 3, 4], dtype='i4')

# printing array and datatype
print('Array:', arr)
print('Datatype:', arr.dtype)
```

**输出:**

```
Array: [1 2 3 4 8 9 5]
Datatype: int32
```

在上面的例子中，整数元素的大小是 4，即 32 字节

**例 3:**

## 蟒蛇 3

```
import numpy as np

# creating and initialising array along
# with datatype and its size 8 i.e. 64bytes
arr = np.array([1, 2, 3, 4], dtype='i8')

# printing array and datatype
print('Array:', arr)
print('Datatype:', arr.dtype)
```

**输出:**

```
Array: [1 2 3 4 8 9 7]
Datatype: int64
```

在这个例子中，元素的大小是 64 字节。

**例 4:**

## 蟒 3

```
import numpy as np

# creating and initialising array along
# with datatype and its size 4 i.e. 32bytes
arr = np.array([1, 2, 3, 4, 8, 9, 7], dtype='f4')

# printing array and datatype
print('Array:', arr)
print('Datatype:', arr.dtype)
```

**输出:**

```
Array: [1\. 2\. 3\. 4\. 8\. 9\. 7.]
Datatype: float32
```

在上面的例子中，数据类型是 float，大小是 32 字节。

**例 5:**

## 蟒 3

```
import numpy as np

# creating and initialising array along
# with datatype and its size 2
arr = np.array([1, 2, 3, 4, 8, 9, 7], dtype='S2')

# printing array and datatype
print('Array:', arr)
print('Datatype:', arr.dtype)
```

**输出:**

```
Array: [b'1' b'2' b'3' b'4' b'8' b'9' b'7']
Datatype: |S2
```

在上面的例子中，数据类型是一个字符串，大小是 2。
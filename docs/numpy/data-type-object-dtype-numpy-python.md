# NumPy Python 中的数据类型对象(数据类型)

> 原文:[https://www . geesforgeks . org/data-type-object-dtype-numpy-python/](https://www.geeksforgeeks.org/data-type-object-dtype-numpy-python/)

每个数组都有一个关联的数据类型(dtype)对象。这个数据类型对象(dtype)告诉我们数组的布局。这意味着它为我们提供了以下信息:

*   数据的类型(整数、浮点、Python 对象等)。)
*   数据大小(字节数)
*   数据的字节顺序(小端或大端)
*   如果数据类型是子数组，它的形状和数据类型是什么？

数组的值存储在一个缓冲区中，这个缓冲区可以看作是一个连续的内存字节块。因此如何解释这些字节是由 dtype 对象给出的。

**1。构造数据类型(dtype)对象:**数据类型对象是 NumPy.dtype 类的实例，可以使用 NumPy.dtype 创建。

**参数:**

*   **对象:**要转换为数据类型对象的对象。
*   **对齐** : bool，可选
    在字段中添加填充，以匹配 C 编译器为类似的 C 结构输出的内容。
*   **复制** : bool，可选
    制作数据类型对象的新副本。如果为 False，结果可能只是对内置数据类型对象的引用。

## 计算机编程语言

```py
# Python Program to create a data type object
import numpy as np

# np.int16 is converted into a data type object.
print(np.dtype(np.int16))
```

**输出:**

```py
int16
```

## 计算机编程语言

```py
# Python Program to create a data type object
# containing a 32 bit big-endian integer
import numpy as np

# i4 represents integer of size 4 byte
# > represents big-endian byte ordering and < represents little-endian encoding.
# dt is a dtype object
dt = np.dtype('>i4')

print("Byte order is:",dt.byteorder)

print("Size is:",dt.itemsize)

print("Data type is:",dt.name)
```

**输出:**

```py
Byte order is: >
Size is: 4
Name of data type is: int32
```

类型说明符(上述中的i4)可以采用不同的形式:

*   b1、i1、i2、i4、i8、u1、u2、u4、u8、f2、f4、f8、c8、c16、a
    (表示指定**字节**长度的字节、整数、无符号整数、浮点、复数和
    固定长度字符串)
*   int8，…，uint8，…，float16，float32，float64，complex64，complex128
    (这次用**位**大小)

**注:**

```py
dtype is different from type. 
```

## 计算机编程语言

```py
# Python program to differentiate
# between type and dtype.
import numpy as np

a = np.array([1])

print("type is: ",type(a))
print("dtype is: ",a.dtype)
```

**输出:**

```py
type is:    
dtype is:  int32
```

**2。具有结构化数组的数据类型对象:**数据类型对象对于创建结构化数组非常有用。结构化数组包含不同类型的数据。结构化数组可以在字段的帮助下访问。
字段就像给对象指定名称。在结构化数组的情况下，数据类型对象也将是结构化的。

## 计算机编程语言

```py
# Python program for demonstrating
# the use of fields
import numpy as np

# A structured data type containing a 16-character string (in field ‘name’) 
# and a sub-array of two 64-bit floating-point number (in field ‘grades’):

dt = np.dtype([('name', np.unicode_, 16), ('grades', np.float64, (2,))])

# Data type of object with field grades
print(dt['grades'])

# Data type of object with field name 
print(dt['name'])
```

**输出:**

```py
('<f8', (2,))
```

## 计算机编程语言

```py
# Python program to demonstrate 
# the use of data type object with structured array.
import numpy as np

dt = np.dtype([('name', np.unicode_, 16), ('grades', np.float64, (2,))])

# x is a structured array with names and marks of students.
# Data type of name of the student is np.unicode_ and 
# data type of marks is np.float(64)
x = np.array([('Sarah', (8.0, 7.0)), ('John', (6.0, 7.0))], dtype=dt)

print(x[1])
print("Grades of John are: ",x[1]['grades'])
print("Names are: ",x['name'])
```

**输出:**

```py
('John', [ 6.,  7.])
Grades of John are:  [ 6\.  7.]
Names are:  ['Sarah' 'John']
```

**参考文献:**

*   [docs.scipy.org](https://docs.scipy.org/doc/numpy/reference/arrays.dtypes.html)
*   [结构化阵列](https://docs.scipy.org/doc/numpy/user/basics.rec.html)

本文由 **Ayushi Asthana** 供稿。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[write.geeksforgeeks.org](https://write.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 review-team@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。
如果你发现任何不正确的地方，或者你想分享更多关于上面讨论的话题的信息，请写评论。
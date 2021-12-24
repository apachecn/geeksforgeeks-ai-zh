# 如何使用 NumPy

在 Python 中创建矢量

> 原文:[https://www . geeksforgeeks . org/如何使用-numpy/](https://www.geeksforgeeks.org/how-to-create-a-vector-in-python-using-numpy/) 创建 python 矢量

**NumPy** 是一个通用的数组处理包。它提供了一个高性能的多维数组对象，以及使用这些数组的工具。它是使用 Python 进行科学计算的基本包。Numpy 基本上用于创建 n 维数组。

**矢量**由分量构成，分量是普通数。我们可以把向量想象成一个数字列表，而向量代数是对列表中的数字进行的运算。换句话说，向量就是一维数组。

为了创建一个向量，我们使用 np.array 方法。

> **语法:** np.array(list)
> **参数:**取一维列表，可以是 1 行 n 列，也可以是 n 行 1 列
> **返回:**返回 numpy.ndarray
> 的向量

**注:**我们也可以用其他方法创建向量，这些方法返回一维数组，例如 np.arange(10)，NP . zero((4，1))给出一维数组，但最合适的方法是将 np.array 与一维列表一起使用。

**创建向量**
在这个例子中，我们将创建一个水平向量和一个垂直向量

## 蟒蛇 3

```
# importing numpy
import numpy as np

# creating a 1-D list (Horizontal)
list1 = [1, 2, 3]

# creating a 1-D list (Vertical)
list2 = [[10],
        [20],
        [30]]

# creating a vector1
# vector as row
vector1 = np.array(list1)

# creating a vector 2
# vector as column
vector2 = np.array(list2)

# showing horizontal vector
print("Horizontal Vector")
print(vector1)

print("----------------")

# showing vertical vector
print("Vertical Vector")
print(vector2)
```

**输出:**

```
Horizontal Vector
[1 2 3]
----------------
Vertical Vector
[[10]
 [20]
 [30]]
```

**基本算术运算:**
在本例中，我们将看到在两个长度相等的向量之间按元素进行算术运算，得到一个长度相同的新向量

## 蟒蛇 3

```
# importing numpy
import numpy as np

# creating a 1-D list (Horizontal)
list1 = [5, 6, 9]

# creating a 1-D list (Horizontal)
list2 = [1, 2, 3]

# creating first vector
vector1 = np.array(list1)

# printing vector1
print("First Vector          : " + str(vector1))

# creating second vector
vector2 = np.array(list2)

# printing vector2
print("Second Vector         : " + str(vector2))

# adding both the vector
# a + b = (a1 + b1, a2 + b2, a3 + b3)
addition = vector1 + vector2

# printing addition vector
print("Vector Addition       : " + str(addition))

# subtracting both the vector
# a - b = (a1 - b1, a2 - b2, a3 - b3)
subtraction = vector1 - vector2

# printing addition vector
print("Vector Subtraction   : " + str(subtraction))

# multiplying  both the vector
# a * b = (a1 * b1, a2 * b2, a3 * b3)
multiplication = vector1 * vector2

# printing multiplication vector
print("Vector Multiplication : " + str(multiplication))

# dividing  both the vector
# a / b = (a1 / b1, a2 / b2, a3 / b3)
division = vector1 / vector2

# printing division vector
print("Vector Division       : " + str(division))
```

**输出:**

```
First Vector: [5 6 9]
Second Vector: [1 2 3]
Vector Addition: [ 6  8 12]
Vector Subtraction: [4 4 6]
Vector Multiplication: [ 5 12 27]
Vector Division: [5 3 3]
```

**向量点积**
在数学中，点积或标量积是取两个等长的数字序列并返回一个数字的代数运算。
为此我们将使用点方法。

## 蟒蛇 3

```
# importing numpy
import numpy as np

# creating a 1-D list (Horizontal)
list1 = [5, 6, 9]

# creating a 1-D list (Horizontal)
list2 = [1, 2, 3]

# creating first vector 
vector1 = np.array(list1)

# printing vector1
print("First Vector  : " + str(vector1))

# creating second vector
vector2 = np.array(list2)

# printing vector2
print("Second Vector : " + str(vector2))

# getting dot product of both the vectors
# a . b = (a1 * b1 + a2 * b2 + a3 * b3)
# a . b = (a1b1 + a2b2 + a3b3)
dot_product = vector1.dot(vector2)

# printing dot product
print("Dot Product   : " + str(dot_product))
```

**输出:**

```
First Vector  : [5 6 9]
Second Vector : [1 2 3]
Dot Product   : 44
```

**向量-标量乘法**
将向量乘以标量叫做标量乘法。要执行标量乘法，我们需要将标量乘以向量的每个分量。

## 蟒蛇 3

```
# importing numpy
import numpy as np

# creating a 1-D list (Horizontal)
list1 = [1, 2, 3]

# creating first vector 
vector = np.array(list1)

# printing vector1
print("Vector  : " + str(vector))

# scalar value 
scalar = 2

# printing scalar value
print("Scalar  : " + str(scalar))

# getting scalar multiplication value
# s * v = (s * v1, s * v2, s * v3)
scalar_mul = vector * scalar

# printing dot product
print("Scalar Multiplication : " + str(scalar_mul))

```

**输出**

```
Vector  : [1 2 3]
Scalar  : 2
Scalar Multiplication : [2 4 6]
```
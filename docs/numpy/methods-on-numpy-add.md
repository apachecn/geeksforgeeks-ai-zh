# numpy . add()上的方法

> 原文:[https://www.geeksforgeeks.org/methods-on-numpy-add/](https://www.geeksforgeeks.org/methods-on-numpy-add/)

**ufunc** 期望一组标量作为输入，并产生一组标量作为输出。通用
函数可以与数学方面相关，例如，加、减、除、乘等。

## numpy.add 上的方法

实际上，通用函数不是函数，而是代表函数的对象。这里我们使用函数–add，它们有两个输入参数并返回一个输出参数(ufunc 的签名不匹配将导致 ValueError。因此这仅适用于二进制通用函数)。

**add 上的四种方法是:**

*   [降低](#reduce)
*   [累计](#accumulate)
*   [外](#outer)
*   减少

在本教程中，我们将详细介绍上述每个函数。

### numpy . ufunc . reduce()

给定的输入数组通过在连续的元素上沿着指定的轴递归地应用通用函数来缩减。
**注:** `add.reduce()`相当于`sum()`

> **语法:** ufunc.reduce(a，轴=0，数据类型=无，out =无，keepdims =假，初始值=，其中=真)
> 
> **参数****:**
> **a(array _ like):**发生处理的数组
> **轴(None 或 int 或 int 的元组，可选):**执行归约的一个或多个轴。默认值为(轴= 0)。轴可以是负的，只要它向后计数。无，在所有轴上执行缩减。整数元组，在多个轴上执行约简。
> **数据类型(数据类型代码，可选):**用于表示中间结果的类型。
> **输出(n 数组，无，或 n 数组和无的元组，可选):**存储结果的位置。如果未提供或无，则返回新分配的数组。
> **保持尺寸(布尔，可选):**如果设置为真，则缩小的轴作为尺寸为 1 的尺寸留在结果中。
> **初始值(标量，可选):**开始归约的值。
> **其中(array_like of bool，可选):**一个布尔数组，它被广播以匹配的维度，并选择要包含在约简中的元素。
> 
> **返回:**T2:否

**示例:**

```py
# Reducing an array using np.add.reduce()

import numpy as np

# Array formation
a = np.arange(10)

# Reduction occurs column-wise with 
# 'int' datatype
b = np.add.reduce(a, dtype = int, axis = 0)
print("The array {0} gets reduced to {1}".format(a, b))
```

**输出**

```py
The array [0 1 2 3 4 5 6 7 8 9] gets reduced to 45
```

### 累计序号()

它将中间结果存储在一个数组中并返回该数组。结果，在加法函数的情况下，相当于调用 cumsum 函数。

> **语法:**ufunc . aggregate(数组，轴=0，数据类型=无，输出=无)
> 
> **参数:**
> **阵(array_like):** 该阵要行动了。
> **轴(int，可选):**应用累加的轴；默认值为零。
> **数据类型(数据类型代码，可选):**用于表示中间结果的数据类型。如果提供了输出数组，则默认为输出数组的数据类型；如果没有提供输出数组，则默认为输入数组的数据类型。
> **out(n 数组，可选):**存储结果的位置。如果未提供，则返回新分配的数组。
> 
> **返回:**T2:否

**示例:**

```py
import numpy as np

# Array formation
a = np.arange(10)

# Cumulative sum of array, column wise,
# float datatype
c = np.add.accumulate(a, axis = 0, dtype = float)

print("The array {0} gets added cumulatively to {1}".format(a, c))
```

**输出**

> 数组[0 1 2 3 4 5 6 7 8 9]被累加到[0。1.3.6.10.15.21.28.36.45.]

### numpy . ufunc . outer()函数

“outer”方法返回一个具有秩的数组，该秩是其两个输入数组的秩之和。该方法应用于所有可能的输入数组元素对。

> **语法:** ufunc.outer(A，B，**kwargs)
> 
> **参数:**
> **A(array_like):** 第一个数组
> **B(array_like):** 第二个数组
> **kwargs(任意):**传递给 ufunc 的参数。
> 
> **返回:**T2:否

**示例:**

```py
# To find the outer of two input arrays
import numpy as np

# Initialization of a 2x2 matrix 
# as first input
a = np.arange(4).reshape(2,2)

# Initialization of an array as
# second input
b = np.arange(3)

# Outer of a & b
z = np.add.outer(b, a)

print("The outer of {0} & {1} is {2}".format(b,a,z))
```

**输出**

```py
The outer of [0 1 2] & [[0 1]
 [2 3]] is [[[0 1]
  [2 3]]

 [[1 2]
  [3 4]]

 [[2 3]
  [4 5]]]
```

### numpy . ufunc . reduceat()

“`reduceat()`”方法需要一个输入数组和一个索引列表作为参数。`reduceat()`方法通过一步一步的程序来执行其操作。我们将分四步来看它的行动。

**示例:**

```py
# Reduceat method example

import numpy as np

a = np.arange(9)
z = np.add.reduceat(a, [1, 4, 2, 8])

print("Reduceat of matrix {} is {}".format(a,z))
```

**输出**

> 矩阵[0 1 2 3 4 5 6 7 8]的约简是[ 6 4 27 8]

**STEP-1**
它涉及指数 1 和 4。该步骤导致索引 1 和 4 之间的阵列元素的操作减少。

```py
import numpy as np

a = np.arange(9)
print("Result of STEP-I is", np.add.reduce(a[0:4]))
```

**输出**

```py
Result of STEP-I is 6
```

**STEP-2**
第二步涉及指数 4 和 2。因为 2 小于 4，所以返回索引 4 处的数组元素:

```py
import numpy as np

a = np.arange(9)
print("Result of STEP-II is", a[4])
```

**输出**

```py
Result of STEP-II is 4
```

**STEP-3**
第三步涉及指数 2 和 8。该步骤导致索引 2 和 8 之间的阵列元素的减少操作:

```py
import numpy as np

a = np.arange(9)
print("Result of STEP-III is", np.add.reduce(a[2:8]))
```

**输出**

```py
Result of STEP-III is 27
```

**STEP-4**
第四步涉及指数 8。该步骤导致从索引 8 到数组末尾的数组元素的减少操作:

```py
import numpy as np

a = np.arange(9)
print("Result of step IV is", np.add.reduce(a[8:]))
```

**输出**

```py
Result of step IV is 8
```

通过完成所有这些步骤，我们得到了' numpy.add.reduceat '的输出。
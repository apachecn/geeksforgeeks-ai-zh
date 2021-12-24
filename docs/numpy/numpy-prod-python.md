# Python 中的 Numpy.prod()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-prod-python/

numpy.prod()返回给定轴上数组元素的乘积。
**语法:**

```
numpy.prod(a, axis=None, dtype=None, out=None, keepdims=)
```

**参数**
**一:阵 _ 象**
其输入数据。
**轴:** None 或 int 或 int 元组，可选
它是执行产品的轴。默认轴是无，它将计算输入数组中所有元素的乘积。如果轴为负，则从最后一个轴到第一个轴计数。
如果 axis 是 int 的元组，则在元组中指定的所有轴上执行乘积，而不是像以前那样在单个轴或所有轴上执行乘积。
**dtype : dtype，其可选的**
是返回数组的类型，也是元素相乘的累加器的类型。默认情况下使用 a 的数据类型，除非 a 的整数数据类型的精度低于默认平台整数。在这种情况下，如果是有符号的，则使用平台整数，而如果是无符号的，则使用与平台整数具有相同精度的无符号整数。
**出:ndarray，其可选的**
备选输出数组中放置结果。它必须具有与预期输出相同的形状，但是如果需要，输出值的类型将被转换。
**保持:布尔，可选**
如果设置为真，则缩小的轴作为尺寸为 1 的尺寸留在结果中。使用此选项，结果将根据输入数组正确广播。
**例 1**

## 计算机编程语言

```
# Python Program illustrating
# working of prod()

import numpy as np
array1 = [1, 2]

# applying function
array2 = np.prod(array1)

print("product", array2)
```

输出:

```
2.0
```

**例 2**T2【一个 2d 阵列

## 计算机编程语言

```
import numpy as np
array1 = [[1., 2.], [3., 4.]]

# applying function
array2 = np.prod(array1)

print("product", array2)
```

输出:

```
24.0
```

**例 3**
空数组的乘积将是中性元素 1:

## 计算机编程语言

```
import numpy as np
array1 = []

# applying function
array2 = np.prod(array1)

print("product", array2)
```

输出:

```
1
```

**示例 4**
通过指定我们相乘的轴

## 计算机编程语言

```
import numpy as np
array1 =[[1, 2], [3, 4]]

# applying function
array2 = np.prod(array1, axis = 1)

print("product", array2)
```

输出:

```
[2, 12]
```

**例 5**
如果 x 的类型是无符号的，那么输出类型会是无符号的平台整数

## 计算机编程语言

```
import numpy as np
x = np.array([1, 2, 3], dtype = np.uint8)

# applying function
 np.prod(x).dtype == np.uint
```

输出:

```
True
```
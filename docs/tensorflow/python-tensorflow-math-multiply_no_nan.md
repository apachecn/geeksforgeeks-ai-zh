# Python–tensorflow . math . multiply _ no _ nan()

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-multiply _ no _ nan/](https://www.geeksforgeeks.org/python-tensorflow-math-multiply_no_nan/)

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 python 库。 **multiply_no_nan()** 用于寻找元素 wise x*y，支持广播，如果 y 为 0 甚至是 x 为无穷大或者 nan，则返回 0。

> **语法:** tf.math.multiply_no_nan(x，y，name)
> 
> **参数:**
> 
> *   **x:** 是输入张量。这个张量允许的数据类型是 bfloat16，half，float32，float64，uint8，int8，uint16，int16，int32，int64，complex64，complex128。
> *   **y:** 是与 x 相同数据类型的输入张量。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**
> 返回一个与 x 相同数据类型的张量

**例 1:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([.2, .5, .7, 1], dtype = tf.float64)
b = tf.constant([.1, .3, 1, 5], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)
print('b: ', b)

# Calculating result
res = tf.math.multiply_no_nan(x = a, y = b)

# Printing the result
print('Result: ', res)
```

**输出:**

```
a:  tf.Tensor([0.2 0.5 0.7 1\. ], shape=(4, ), dtype=float64)
b:  tf.Tensor([0.1 0.3 1\.  5\. ], shape=(4, ), dtype=float64)
Result:  tf.Tensor([0.02 0.15 0.7  5\.  ], shape=(4, ), dtype=float64)

```

**例 2:** 复数乘法

## 蟒蛇 3

```
# importing the library
import tensorflow as tf
import numpy as np

# Initializing the input tensor
a = tf.constant([-2, -5, np.inf, np.nan], dtype = tf.float64)
b = tf.constant([-1, -6, 0, 0], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)
print('b: ', b)

# Calculating result
res = tf.math.multiply_no_nan(x = a, y = b)

# Printing the result
print('Result: ', res)
```

**输出:**

```
a:  tf.Tensor([-2\. -5\. inf nan], shape=(4, ), dtype=float64)
b:  tf.Tensor([-1\. -6\.  0\.  0.], shape=(4, ), dtype=float64)
Result:  tf.Tensor([ 2\. 30\.  0\.  0.], shape=(4, ), dtype=float64)

```
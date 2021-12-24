# Python–tensorflow . math . multiply()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-multiply/

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 python 库。 **multiply()** 用于寻找 element wise x*y，支持广播。

> **语法:** tf.math .乘法(x，y，name)
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
res = tf.math.multiply(x = a, y = b)

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

# Initializing the input tensor
a = tf.constant([-2 + 3j, -5 + 4j, 7 + 2j, 1 + 7j], dtype = tf.complex128)
b = tf.constant([-1 + 2j, -6 + 8j, 8 + 2j, 0 + 1j], dtype = tf.complex128)

# Printing the input tensor
print('a: ', a)
print('b: ', b)

# Calculating result
res = tf.math.multiply(x = a, y = b)

# Printing the result
print('Result: ', res)
```

**输出:**

```
a:  tf.Tensor([-2.+3.j -5.+4.j  7.+2.j  1.+7.j], shape=(4, ), dtype=complex128)
b:  tf.Tensor([-1.+2.j -6.+8.j  8.+2.j  0.+1.j], shape=(4, ), dtype=complex128)
Result:  tf.Tensor([-4\. -7.j -2.-64.j 52.+30.j -7\. +1.j], shape=(4, ), dtype=complex128)

```
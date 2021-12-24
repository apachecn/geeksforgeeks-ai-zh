# Python–tensorflow . math .倒数 _no_nan()

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-倒数 _no_nan/](https://www.geeksforgeeks.org/python-tensorflow-math-reciprocal_no_nan/)

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 python 库。**倒数 _no_nan()** 用于求 x 的元素安全倒数，即如果 x 为 0，则其倒数也为 0。

> **语法:** tf.math .倒数 _no_nan(x，name)
> 
> **参数:**
> 
> *   **x:** 是输入张量。这个张量允许的数据类型是 bfloat16，half，float32，float64，int32，int64，complex64，complex128。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**
> 它返回一个与 x 相同类型的张量。

**例 1:** 本例使用实张量。

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([0, 2, -3, -4], dtype = tf.float64)

# Printing the input tensor
print('Input: ', a)

# Calculating result
res = tf.math.reciprocal_no_nan(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```
Input:  tf.Tensor([ 0\.  2\. -3\. -4.], shape=(4, ), dtype=float64)
Result:  tf.Tensor([ 0\.          0.5        -0.33333333 -0.25      ], shape=(4, ), dtype=float64)

```

**例 2:** 本例使用复张量。

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([0 + 0j, 2-5j, -3 + 7j, -4-8j], dtype = tf.complex128)

# Printing the input tensor
print('Input: ', a)

# Calculating result
res = tf.math.reciprocal_no_nan( a)

# Printing the result
print('Result: ', res)
```

**输出:**

```
Input:  tf.Tensor([ 0.+0.j  2.-5.j -3.+7.j -4.-8.j], shape=(4, ), dtype=complex128)
Result:  tf.Tensor(
[ 0\.        +0.j          0.06896552+0.17241379j -0.05172414-0.12068966j
 -0.05      +0.1j       ], shape=(4, ), dtype=complex128)
```
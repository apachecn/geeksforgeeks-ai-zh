# Python–tensorflow . math . zero _ fraction()

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-zero _ fraction/](https://www.geeksforgeeks.org/python-tensorflow-math-zero_fraction/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**zero_fraction()** 用于查找值中零的分数。

> **语法:** tensorflow.math.softplus(值，名称)
> 
> **参数:**
> 
> *   **值:**是数值型张量。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**返回值中零的分数，数据类型为 float32。

**例 1:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([ 5, 0, 9, 15], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)

# Calculating result
res = tf.math.zero_fraction(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```
a:  tf.Tensor([ 5\.  0\.  9\. 15.], shape=(4, ), dtype=float64)
Result:  tf.Tensor(0.25, shape=(), dtype=float32)

```

**例 2:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([ 5 + 3j, 0 + 0j, 9-6j, 0 + 0j], dtype = tf.complex128)

# Printing the input tensor
print('a: ', a)

# Calculating result
res = tf.math.zero_fraction(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```
a:  tf.Tensor([5.+3.j 0.+0.j 9.-6.j 0.+0.j], shape=(4, ), dtype=complex128)
Result:  tf.Tensor(0.5, shape=(), dtype=float32)
```
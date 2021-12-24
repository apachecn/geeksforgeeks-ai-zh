# Python–tensorflow . math . reduce _ variance()

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-reduce _ variance/](https://www.geeksforgeeks.org/python-tensorflow-math-reduce_variance/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**reduce_variance()** 用于寻找元素在张量维度上的方差。

> **语法:**tensorflow . math . reduce _ variance(input _ tensor，axis，keepdims，name)
> 
> **参数:**
> 
> *   **input_tensor:** 是要约简的数值张量。
> *   **轴(可选):**表示要缩小的尺寸。它的值应该在[-rank(input_tensor)，rank(input _ tensor)]范围内。如果没有给出这个值，所有的维度都将减少。
> *   **保持(可选):**默认值为假。如果设置为真，它将保留长度为 1 的缩小尺寸。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**返回张量。

**例 1:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([1, 2, 3, 4], dtype = tf.float64)

# Printing the input tensor
print('Input: ', a)

# Calculating result
res = tf.math.reduce_variance(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
Input:  tf.Tensor([1\. 2\. 3\. 4.], shape=(4, ), dtype=float64)
Result:  tf.Tensor(1.25, shape=(), dtype=float64)
```

**例 2:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([[1, 2], [3, 4]], dtype = tf.float64)

# Printing the input tensor
print('Input: ', a)

# Calculating result
res = tf.math.reduce_variance(a, axis = 1, keepdims = True)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
Input:  tf.Tensor(
[[1\. 2.]
 [3\. 4.]], shape=(2, 2), dtype=float64)
Result:  tf.Tensor(
[[0.25]
 [0.25]], shape=(2, 1), dtype=float64)
```
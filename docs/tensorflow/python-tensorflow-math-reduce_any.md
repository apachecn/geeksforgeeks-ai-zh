# Python–tensorflow . math . reduce _ any()

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-reduce _ any/](https://www.geeksforgeeks.org/python-tensorflow-math-reduce_any/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**reduce_any()** 用于计算跨张量维度的元素的“逻辑或”。

> **语法:**tensorflow . math . reduce _ any(input _ tensor，axis，keepdims，name)
> 
> **参数:**
> 
> *   **input_tensor:** 是要约简的布尔张量。
> *   **轴(可选):**表示要缩小的尺寸。它的值应该在[-rank(input_tensor)，rank(input _ tensor)]范围内。如果没有给出这个值，所有的维度都将减少。
> *   **保持(可选):**默认值为假。如果设置为真，它将保留长度为 1 的缩小尺寸。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**返回张量。

**例 1:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([True, False, False, True], dtype = tf.bool)

# Printing the input tensor
print('Input: ', a)

# Calculating result
res = tf.math.reduce_any(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```
Input:  tf.Tensor([ True False False  True], shape=(4, ), dtype=bool)
Result:  tf.Tensor(True, shape=(), dtype=bool)
```

**例 2:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([[True, False], [False, True]], dtype = tf.bool)

# Printing the input tensor
print('Input: ', a)

# Calculating result
res = tf.math.reduce_any(a, axis = 1, keepdims = True)

# Printing the result
print('Result: ', res)
```

**输出:**

```
Input:  tf.Tensor(
[[ True False]
 [False  True]], shape=(2, 2), dtype=bool)
Result:  tf.Tensor(
[[ True]
 [ True]], shape=(2, 1), dtype=bool)
```
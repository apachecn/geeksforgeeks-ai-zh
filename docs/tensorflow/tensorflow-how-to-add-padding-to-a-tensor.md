# 张量流–如何给张量添加填充

> 原文:[https://www . geesforgeks . org/tensorflow-如何将填充添加到张量/](https://www.geeksforgeeks.org/tensorflow-how-to-add-padding-to-a-tensor/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

填充意味着在张量值之前和之后添加值。

> **使用的方法:**
> 
> *   **tf.pad:** 该方法接受输入张量和带有其他可选参数的填充张量，并返回一个添加了填充且类型与输入张量相同的张量。填充张量是具有形状(n，2)的张量。

**示例 1:** 该示例使用恒定填充模式，即所有填充索引处的值都将是恒定的。

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the Input
input = tf.constant([[1, 2], [3, 4]])
padding = tf.constant([[2, 2], [2, 2]])

# Printing the Input
print("Input: ", input)
print("Padding: ", padding)

# Generating padded Tensor
res = tf.pad(input, padding, mode ='CONSTANT')

# Printing the resulting Tensors
print("Res: ", res )
```

**输出:**

```py
Input:  tf.Tensor(
[[1 2]
 [3 4]], shape=(2, 2), dtype=int32)
Padding:  tf.Tensor(
[[2 2]
 [2 2]], shape=(2, 2), dtype=int32)
Res:  tf.Tensor(
[[0 0 0 0 0 0]
 [0 0 0 0 0 0]
 [0 0 1 2 0 0]
 [0 0 3 4 0 0]
 [0 0 0 0 0 0]
 [0 0 0 0 0 0]], shape=(6, 6), dtype=int32)

```

**示例 2:** 本示例使用 REFLECT 填充模式。要使此模式工作，填充[D，0]和填充[D，1]必须小于或等于 tensor . dim _ size(D)–1。

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the Input
input = tf.constant([[1, 2, 5], [3, 4, 6]])
padding = tf.constant([[1, 1], [2, 2]])

# Printing the Input
print("Input: ", input)
print("Padding: ", padding)

# Generating padded Tensor
res = tf.pad(input, padding, mode ='REFLECT')

# Printing the resulting Tensors
print("Res: ", res )
```

**输出:**

```py
Input:  tf.Tensor(
[[1 2 5]
 [3 4 6]], shape=(2, 3), dtype=int32)
Padding:  tf.Tensor(
[[1 1]
 [2 2]], shape=(2, 2), dtype=int32)
Res:  tf.Tensor(
[[6 4 3 4 6 4 3]
 [5 2 1 2 5 2 1]
 [6 4 3 4 6 4 3]
 [5 2 1 2 5 2 1]], shape=(4, 7), dtype=int32)

```
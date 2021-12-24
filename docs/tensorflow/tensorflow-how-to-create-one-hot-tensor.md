# 张量流–如何创建一个热张量

> 原文:[https://www . geesforgeks . org/tensorflow-如何创建一个热张量/](https://www.geeksforgeeks.org/tensorflow-how-to-create-one-hot-tensor/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

一个热点张量是这样一个张量，其中所有的值都在 i =j 和 I 的指数上！=j 相同。

> **使用的方法:**
> 
> *   **one_hot:** 该方法接受一个指数张量，一个定义一个 hot 维度深度的标量，并返回一个默认开值为 1、关值为 0 的 one hot 张量。这些开和关值可以修改。

**例 1:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the Input
indices = tf.constant([1, 2, 3])

# Printing the Input
print("Indices: ", indices)

# Generating one hot Tensor
res = tf.one_hot(indices, depth = 3)

# Printing the resulting Tensors
print("Res: ", res )
```

**输出:**

```py
Indices:  tf.Tensor([1 2 3], shape=(3, ), dtype=int32)
Res:  tf.Tensor(
[[0\. 1\. 0.]
 [0\. 0\. 1.]
 [0\. 0\. 0.]], shape=(3, 3), dtype=float32)

```

**示例 2:** 该示例明确定义了一个热张量的开和关值。

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the Input
indices = tf.constant([1, 2, 3])

# Printing the Input
print("Indices: ", indices)

# Generating one hot Tensor
res = tf.one_hot(indices, depth = 3, on_value = 3, off_value =-1)

# Printing the resulting Tensors
print("Res: ", res )
```

**输出:**

```py
Indices:  tf.Tensor([1 2 3], shape=(3, ), dtype=int32)
Res:  tf.Tensor(
[[-1  3 -1]
 [-1 -1  3]
 [-1 -1 -1]], shape=(3, 3), dtype=int32)

```
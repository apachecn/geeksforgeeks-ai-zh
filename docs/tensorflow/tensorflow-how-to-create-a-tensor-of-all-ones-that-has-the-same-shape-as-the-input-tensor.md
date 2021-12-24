# 张量流–如何创建与输入张量形状相同的张量

> 原文:[https://www . geesforgeks . org/tensorflow-如何创建与输入张量具有相同形状的全一张量/](https://www.geeksforgeeks.org/tensorflow-how-to-create-a-tensor-of-all-ones-that-has-the-same-shape-as-the-input-tensor/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

> **使用的方法:**
> 
> *   **one _ like:**该方法接受一个张量作为输入，并返回一个具有相同形状的张量，所有值都设置为 1。

**例 1:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the Input
input = tf.constant([[1, 2, 3], [4, 5, 6]])

# Generating Tensor with having all values as 1
res = tf.ones_like(input)

# Printing the resulting Tensors
print("Res: ", res )
```

**输出:**

```
Res:  tf.Tensor(
[[1 1 1]
 [1 1 1]], shape=(2, 3), dtype=int32)

```

**示例 2:** 该示例明确指定了结果张量的类型。

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the Input
input = tf.constant([[1, 2, 3], [4, 5, 6]])

# Printing the Input
print("Input: ", input)

# Generating Tensor with having all values as 1
res = tf.ones_like(input, dtype = tf.float64)

# Printing the resulting Tensors
print("Res: ", res )
```

**输出:**

```
Input:  tf.Tensor(
[[1 2 3]
 [4 5 6]], shape=(2, 3), dtype=int32)
Res:  tf.Tensor(
[[1\. 1\. 1.]
 [1\. 1\. 1.]], shape=(2, 3), dtype=float64)

```
# 张量流–如何创建所有元素都设置为一的张量

> 原文:[https://www . geesforgeks . org/tensorflow-如何创建一个所有元素集为一的张量/](https://www.geeksforgeeks.org/tensorflow-how-to-create-a-tensor-with-all-elements-set-to-one/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

> **使用的方法:**
> 
> *   [T0】 TF. one: 【T1] This method accepts shapes and types and returns tensors of given shapes and types, all of which are set to 1.
> *   **TF. fill:** This method accepts shapes, values and types, and returns tensors of given shapes and types, all values are set to values.

**示例 1:** 本示例使用 ones()方法创建所有元素都设置为 1 的张量。

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Generating a Tensor of shape (2, 3)
res = tf.ones(shape = (2, 3))

# Printing the resulting Tensors
print("Res: ", res )
```

**输出:**

```

Res:  tf.Tensor(
[[1\. 1\. 1.]
 [1\. 1\. 1.]], shape=(2, 3), dtype=float32)

```

**示例 2:** 本示例使用 fill()方法，值= 1，创建一个所有元素都设置为 1 的张量。

## 蟒 3

```
# importing the library
import tensorflow as tf

# Generating a Tensor of shape (2, 3)
res = tf.fill(dims = (2, 3), value = 1)

# Printing the resulting Tensors
print("Res: ", res )
```

**输出:**

```

Res:  tf.Tensor(
[[1 1 1]
 [1 1 1]], shape=(2, 3), dtype=int32)

```
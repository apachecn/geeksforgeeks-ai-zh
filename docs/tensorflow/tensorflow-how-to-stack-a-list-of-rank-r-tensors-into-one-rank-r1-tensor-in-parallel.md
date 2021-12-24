# 张量流–如何将一列秩-R 张量并行堆叠成一个秩-(R+1)张量

> 原文:[https://www . geeksforgeeks . org/tensorflow-如何将一列秩 r-tensors 堆叠成一列秩 R1-张量并行/](https://www.geeksforgeeks.org/tensorflow-how-to-stack-a-list-of-rank-r-tensors-into-one-rank-r1-tensor-in-parallel/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

张量流提供内置方法，将一列秩为-R 的张量并行堆叠成一个秩为-(R+1)的张量。

> **使用的方法:**
> 
> *   **parallel_stack:** 这个方法接受一个张量列表，并返回一个张量，所有的值都是并行堆叠的。这些方法将输入片段复制到可用的输出中。
> *   **堆叠:**该方法接受张量列表，即值应该沿着哪个轴堆叠，并返回所有值都堆叠的张量。

**例 1:** 本例采用叠加法叠加张量。

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the Input
x = tf.constant([1, 2, 3])
y = tf.constant([4, 5, 6])
z = tf.constant([7, 8, 9])

# Printing the Input
print("x: ", x)
print("y: ", y)
print("z: ", z)

# Stacking Tensors
res = tf.stack(values =[x, y, z], axis = 0)

# Printing the resulting Tensor
print("Res: ", res )
```

**输出:**

```py

x:  tf.Tensor([1 2 3], shape=(3, ), dtype=int32)
y:  tf.Tensor([4 5 6], shape=(3, ), dtype=int32)
z:  tf.Tensor([7 8 9], shape=(3, ), dtype=int32)
Res:  tf.Tensor(
[[1 2 3]
 [4 5 6]
 [7 8 9]], shape=(3, 3), dtype=int32)

```

**示例 2:** 本示例使用 parallel_stack 方法对输入张量进行堆栈。

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the Input
x = tf.constant([1, 2, 3])
y = tf.constant([4, 5, 6])
z = tf.constant([7, 8, 9])

# Printing the Input
print("x: ", x)
print("y: ", y)
print("z: ", z)

# Stacking Tensors
res = tf.parallel_stack(values =[x, y, z])

# Printing the resulting Tensor
print("Res: ", res )
```

**输出:**

```py
x:  tf.Tensor([1 2 3], shape=(3, ), dtype=int32)
y:  tf.Tensor([4 5 6], shape=(3, ), dtype=int32)
z:  tf.Tensor([7 8 9], shape=(3, ), dtype=int32)
Res:  tf.Tensor(
[[1 2 3]
 [4 5 6]
 [7 8 9]], shape=(3, 3), dtype=int32)
```
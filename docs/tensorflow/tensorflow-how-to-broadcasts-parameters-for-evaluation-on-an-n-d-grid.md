# 张量流–如何在二维网格上广播评估参数

> 原文:[https://www . geesforgeks . org/tensorflow-how-to-broadcasts-an-n-d-grid 上的评估参数/](https://www.geeksforgeeks.org/tensorflow-how-to-broadcasts-parameters-for-evaluation-on-an-n-d-grid/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

在使用 TensorFlow 时，有些操作会自动广播参数，有些时候我们必须显式广播参数。为了显式地广播参数，使用了网格方法。

> **使用的方法:**
> 
> *   **网格网格:**该方法用于在 N-D 网格上广播评估参数。它接受秩为 1 的张量，并将所有张量广播到相同的形状，并返回秩为 N 的 N 个张量的列表。该方法的默认索引是“xy”。

**示例 1:** 在该方法中，使用默认索引。

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing Input
x = [1, 2, 3]
y = [4, 5, 6, 7]

# Printing the Input
print("x: ", x)
print("y: ", y)

# Broadcasting the Tensors
X, Y = tf.meshgrid(x, y)

# Printing the resulting Tensors
print("X: ", X)
print("Y: ", Y)
```

**输出:**

```
x:  [1, 2, 3]
y:  [4, 5, 6, 7]
X:  tf.Tensor(
[[1 2 3]
 [1 2 3]
 [1 2 3]
 [1 2 3]], shape=(4, 3), dtype=int32)
Y:  tf.Tensor(
[[4 4 4]
 [5 5 5]
 [6 6 6]
 [7 7 7]], shape=(4, 3), dtype=int32)

```

**例 2:** 在本例中，索引改为‘ij’。

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing Input
x = [1, 2, 3]
y = [4, 5, 6, 7]

# Printing the Input
print("x: ", x)
print("y: ", y)

# Broadcasting the Tensors
X, Y = tf.meshgrid(x, y, indexing = 'ij')

# Printing the resulting Tensors
print("X: ", X)
print("Y: ", Y)
```

**输出:**

```
x:  [1, 2, 3]
y:  [4, 5, 6, 7]
X:  tf.Tensor(
[[1 1 1 1]
 [2 2 2 2]
 [3 3 3 3]], shape=(3, 4), dtype=int32)
Y:  tf.Tensor(
[[4 5 6 7]
 [4 5 6 7]
 [4 5 6 7]], shape=(3, 4), dtype=int32)

```
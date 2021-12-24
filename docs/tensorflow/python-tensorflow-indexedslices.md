# python–tensorlow . index dslices()

> 原文:[https://www . geesforgeks . org/python-tensorflow-indexed slices/](https://www.geeksforgeeks.org/python-tensorflow-indexedslices/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**IndexedSlices()** 用于在给定的索引下寻找一组张量切片的稀疏表示。

> **语法:**张量流。索引策略(值、索引、密集形状=无)
> 
> **参数:**
> 
> *   **值:**它是任何数据类型的张量。
> *   **指数:**它是一维张量。
> 
> **返回:**返回一个 IndexedSlices 对象。

**例 1:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input
data = tf.constant([1, 2, 3])

# Printing the input
print('data: ', data)

# Calculating result
res = tf.IndexedSlices(data, [0])

# Printing the result
print('res: ', res)
```

**输出:**

```py

data:  tf.Tensor([1 2 3], shape=(3, ), dtype=int32)
res:  IndexedSlices(indices=[0], values=tf.Tensor([1 2 3], shape=(3, ), dtype=int32))

```

**例 2:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input
data = tf.constant([[1, 2, 3], [4, 5, 6]])

# Printing the input
print('data: ', data)

# Calculating result
res = tf.IndexedSlices(data, [0])

# Printing the result
print('res: ', res)
```

**输出:**

```py

data:  tf.Tensor(
[[1 2 3]
 [4 5 6]], shape=(2, 3), dtype=int32)
res:  IndexedSlices(indices=[0], values=tf.Tensor(
[[1 2 3]
 [4 5 6]], shape=(2, 3), dtype=int32))

```
# Python–张量流。索引切片形状属性

> 原文:[https://www . geesforgeks . org/python-tensorflow-indexed slices-shape-attribute/](https://www.geeksforgeeks.org/python-tensorflow-indexedslices-shape-attribute/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**形状**用来得到张量流。张量形状表示稠密张量的形状。

> **语法:**张量流。索引的策略。形状
> 
> **返回:**返回张量流。张量形状表示稠密张量的形状。

**例 1:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input
data = tf.constant([[1, 2, 3], [4, 5, 6]])

# Printing the input
print('data: ', data)

# Calculating result
res = tf.IndexedSlices(data, [0], tf.constant([1, 2]))

# Finding Shape
shape = res.shape

# Printing the result
print('Shape: ', shape)
```

**输出:**

```py

data:  tf.Tensor(
[[1 2 3]
 [4 5 6]], shape=(2, 3), dtype=int32)
Shape:  (1, 2)

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
res = tf.IndexedSlices(data, [0], tf.constant([1]))

# Finding Shape
shape = res.shape

# Printing the result
print('Shape: ', shape)
```

**输出:**

```py

data:  tf.Tensor(
[[1 2 3]
 [4 5 6]], shape=(2, 3), dtype=int32)
Shape:  (1, )

```
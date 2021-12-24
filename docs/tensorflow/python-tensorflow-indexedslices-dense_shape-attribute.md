# Python–张量流。索引碎片密集形状属性

> 原文:[https://www . geesforgeks . org/python-tensorflow-indexed slices-dense _ shape-attribute/](https://www.geeksforgeeks.org/python-tensorflow-indexedslices-dense_shape-attribute/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**稠密 _ 形状**返回一个包含相应稠密张量形状的一维张量。

> **语法:**张量流。IndexedSlices .密集形状
> 
> **返回:**返回一维张量。

**例 1:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input
data = tf.constant([1, 2, 3])

# Printing the input
print('data: ', data)

# Calculating result
res = tf.IndexedSlices(data, [0], 2)

# Finding dense shape
dense = res.dense_shape

# Printing the result
print('dense shape: ', dense)
```

**输出:**

```
data:  tf.Tensor([1 2 3], shape=(3, ), dtype=int32)
dense shape:  2

```

**例 2:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input
data = tf.constant([1, 2, 3])

# Printing the input
print('data: ', data)

# Calculating result
res = tf.IndexedSlices(data, [0])

# Finding dense shape
dense = res.dense_shape

# Printing the result
print('dense shape: ', dense)
```

**输出:**

```
data:  tf.Tensor([1 2 3], shape=(3, ), dtype=int32)
dense shape:  None

```
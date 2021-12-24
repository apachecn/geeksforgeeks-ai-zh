# Python–张量流。索引策略.索引属性

> 原文:[https://www . geesforgeks . org/python-tensorflow-indexed slices-indexes-attribute/](https://www.geeksforgeeks.org/python-tensorflow-indexedslices-indices-attribute/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**索引**用于查找切片的索引。

> **语法:**张量流。IndexedSlices.indices
> 
> **返回:**返回包含切片索引的一维张量。

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
res = tf.IndexedSlices(data, [0])

# Finding Graph 
indices = res.indices

# Printing the result
print('Indices: ', indices)
```

**输出:**

```

data:  tf.Tensor([1 2 3], shape=(3, ), dtype=int32)
Indices:  [0]

```

**例 2:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input
data = tf.constant([[1, 2, 3], [4, 5, 6]])

# Printing the input
print('data: ', data)

# Calculating result
res = tf.IndexedSlices(data, [0, 1])

# Finding Graph 
indices = res.indices

# Printing the result
print('Indices: ', indices)
```

**输出:**

```

data:  tf.Tensor(
[[1 2 3]
 [4 5 6]], shape=(2, 3), dtype=int32)
Indices:  [0, 1]

```
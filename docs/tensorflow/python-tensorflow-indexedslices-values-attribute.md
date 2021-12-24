# Python–张量流。索引的策略值属性

> 原文:[https://www . geesforgeks . org/python-tensorflow-indexed slices-values-attribute/](https://www.geeksforgeeks.org/python-tensorflow-indexedslices-values-attribute/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**值**用于获取切片的值。

> **语法:**张量流。IndexedSlices.values
> 
> **返回:**返回包含切片值的张量。

**例 1:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input
data = tf.constant([[1, 2, 3], [4, 5, 6]])

# Printing the input
print('data: ', data)

# Calculating result
res = tf.IndexedSlices(data, [1])

# Finding values
values = res.values

# Printing the result
print('Values: ', values)
```

**输出:**

```
data:  tf.Tensor(
[[1 2 3]
 [4 5 6]], shape=(2, 3), dtype=int32)
Values:  tf.Tensor(
[[1 2 3]
 [4 5 6]], shape=(2, 3), dtype=int32)

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
res = tf.IndexedSlices(data, [1])

# Finding values
values = res.values

# Printing the result
print('Values: ', values)
```

**输出:**

```
data:  tf.Tensor([1 2 3], shape=(3, ), dtype=int32)
Values:  tf.Tensor([1 2 3], shape=(3, ), dtype=int32)

```
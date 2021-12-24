# Python–张量流。设备属性

> 原文:[https://www . geesforgeks . org/python-tensorflow-indexed slices-device-attribute/](https://www.geeksforgeeks.org/python-tensorflow-indexedslices-device-attribute/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**设备**用于查找将要生成值的设备的名称。

> **语法:**张量流。索引的策略。设备
> 
> **返回:**返回设备名称。

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

# Finding device name 
device = res.device

# Printing the result
print('device: ', device)
```

**输出:**

```

data:  tf.Tensor([1 2 3], shape=(3, ), dtype=int32)
device:  /job:localhost/replica:0/task:0/device:CPU:0

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
res = tf.IndexedSlices(data, [0])

# Finding device name 
device = res.device

# Printing the result
print('device: ', device)
```

**输出:**

```

data:  tf.Tensor(
[[1 2 3]
 [4 5 6]], shape=(2, 3), dtype=int32)
device:  /job:localhost/replica:0/task:0/device:CPU:0

```
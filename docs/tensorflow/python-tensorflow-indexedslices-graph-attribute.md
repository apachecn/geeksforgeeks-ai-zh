# Python–张量流。索引策略图属性

> 原文:[https://www . geesforgeks . org/python-tensorflow-indexed slices-graph-attribute/](https://www.geeksforgeeks.org/python-tensorflow-indexedslices-graph-attribute/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**图形**用于查找包含值、索引和形状张量的图形。

> **语法:**张量流。索引策略.图表
> 
> **返回:**它返回一个图形实例。

**例 1:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input
data = tf.constant([[1, 2, 3], [4, 5, 6]], dtype = tf.float32)

# Printing the input
print('data: ', data)

# Calculating result
res = tf.IndexedSlices(data, [0])

# Finding Graph
@tf.function
def gfg(): 
  tf.compat.v1.disable_eager_execution()

  graph = res.graph

  # Printing the result
  print('graph: ', graph)

gfg()
```

**输出:**

```py

data:  Tensor("Const_1:0", shape=(2, 3), dtype=float32)
graph:  <tensorflow.python.framework.ops.Graph object at 0x7f2eeda9e630>

<tf.Operation 'PartitionedCall_1' type=PartitionedCall>

```

**例 2:**

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

# Finding Graph 
graph = res.graph

# Printing the result
print('graph: ', graph)
```

**输出:**

```py

data:  Tensor("Const_6:0", shape=(3, ), dtype=int32)
graph:  <tensorflow.python.framework.ops.Graph object at 0x7f2eeda9e630>

```
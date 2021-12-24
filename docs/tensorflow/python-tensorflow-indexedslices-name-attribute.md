# Python–张量流。索引策略名称属性

> 原文:[https://www . geesforgeks . org/python-tensorflow-indexed slices-name-attribute/](https://www.geeksforgeeks.org/python-tensorflow-indexedslices-name-attribute/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**名称**用于查找索引切片的名称。这仅在紧急执行被禁用时有效。

> **语法:**张量流。IndexedSlices.name
> 
> **返回:**返回索引策略的名称。

**示例 1:** 在此示例中，启用了紧急执行，因此会引发属性错误。

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input
data = tf.constant([[1, 2, 3], [4, 5, 6]])

# Printing the input
print('data: ', data)

# Calculating result
res = tf.IndexedSlices(data, [0], 1)

# Finding name
name = res.name

# Printing the result
print('Name: ', name)
```

**输出:**

```py

data:  tf.Tensor(
[[1 2 3]
 [4 5 6]], shape=(2, 3), dtype=int32)

---------------------------------------------------------------------------

AttributeError                            Traceback (most recent call last)

<ipython-input-7-f07b895be576> in <module>()
     12 
     13 # Finding name
---> 14 name = res.name
     15 
     16 # Printing the result

1 frames

/usr/local/lib/python3.6/dist-packages/tensorflow/python/framework/ops.py in name(self)
   1121   def name(self):
   1122     raise AttributeError(
-> 1123         "Tensor.name is meaningless when eager execution is enabled.")
   1124 
   1125   @property

AttributeError: Tensor.name is meaningless when eager execution is enabled.

```

**示例 2:** 在此示例中，禁用了紧急执行。

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input
data = tf.constant([[1, 2, 3], [4, 5, 6]])

# Printing the input
print('data: ', data)

# Calculating result
res = tf.IndexedSlices(data, [0], 1)

# Finding name
name = res.name

# Printing the result
print('Name: ', name)
```

**输出:**

```py

data:  Tensor("Const_13:0", shape=(2, 3), dtype=int32)
Name:  Const_13:0

```
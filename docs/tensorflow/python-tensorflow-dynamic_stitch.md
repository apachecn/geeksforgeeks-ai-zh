# Python–tensorflow . dynamic _ stitch()

> 原文:[https://www . geesforgeks . org/python-tensorflow-dynamic _ stitch/](https://www.geeksforgeeks.org/python-tensorflow-dynamic_stitch/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**dynamic_stitch()** 用于将多个张量合并为单个张量。

> **语法:** tensorflow.dynamic_stitch(索引、数据、名称)
> 
> **参数:**
> 
> *   **索引:**它是具有最小 1 张量的张量列表，每个张量都具有 dtype int32。
> *   **数据:**是与指数长度相同的张量列表。
> *   **名称(可选):**定义操作的名称。
> 
> **结果:**
> 
> 它返回与数据相同数据类型的张量。

**例 1:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input
indices = [[0, 1, 5], [2, 4, 3, 6]]
data = [[1, 2, 3], [4, 5, 6, 7]]

# Printing the input
print('indices:', indices)
print('data: ', data)

# Calculating result
x = tf.dynamic_stitch(indices, data)

# Printing the result
print('x: ', x)
```

**输出:**

```

indices: [[0, 1, 5], [2, 4, 3, 6]]
data:  [[1, 2, 3], [4, 5, 6, 7]]
x:  tf.Tensor([1 2 4 6 5 3 7], shape=(7, ), dtype=int32)

```

**例 2:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input
indices = [[0, 1, 6], [5, 4, 3]]
data = [[1, 2, 3], [4, 5, 6]]

# Printing the input
print('indices:', indices)
print('data: ', data)

# Calculating result
x = tf.dynamic_stitch(indices, data)

# Printing the result
print('x: ', x)
```

**输出:**

```

indices: [[0, 1, 2], [5, 4, 3]]
data:  [[1, 2, 3], [4, 5, 6]]
x:  tf.Tensor([1 2 3 6 5 4], shape=(6, ), dtype=int32)

```
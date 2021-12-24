# Python–tensorflow . dynamic _ partition()

> 原文:[https://www . geesforgeks . org/python-tensorflow-dynamic _ partition/](https://www.geeksforgeeks.org/python-tensorflow-dynamic_partition/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**dynamic_partition()** 用于将数据划分为若干分区。

> **语法:**tensorflow . dynamic _ partition(数据、分区、num_partitions、名称)
> 
> **参数:**
> 
> *   **数据:**需要分区的是输入张量。
> *   **分区:**是 int32 类型的 Tensor，它的数据应该在[0，num _ partitions 范围内。
> *   **num_partitions:** 定义分区的数量。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**
> 
> 它返回一个包含 num_partitions 项的张量列表。列表中的每个张量都有与数据相同的数据类型。

**示例 1:** 将数据划分为两个分区

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input
data = [1, 2, 3, 4, 5]
num_partitions = 2
partitions = [0, 0, 1, 0, 1]

# Printing the input
print('data: ', data)
print('partitions:', partitions)
print('num_partitions:', num_partitions)

# Calculating result
x = tf.dynamic_partition(data, partitions, num_partitions)

# Printing the result
print('x[0]: ', x[0])
print('x[1]: ', x[1])
```

**输出:**

```
data:  [1, 2, 3, 4, 5]
partitions: [0, 0, 1, 0, 1]
num_partitions: 2
x[0]:  tf.Tensor([1 2 4], shape=(3, ), dtype=int32)
x[1]:  tf.Tensor([3 5], shape=(2, ), dtype=int32)

```

**例 2:** 分成 3 个张量

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input
data = [1, 2, 3, 4, 5, 6, 7]
num_partitions = 3
partitions = [0, 2, 1, 0, 1, 2, 2]

# Printing the input
print('data: ', data)
print('partitions:', partitions)
print('num_partitions:', num_partitions)

# Calculating result
x = tf.dynamic_partition(data, partitions, num_partitions)

# Printing the result
print('x[0]: ', x[0])
print('x[1]: ', x[1])
print('x[2]: ', x[2])
```

**输出:**

```
data:  [1, 2, 3, 4, 5, 6, 7]
partitions: [0, 2, 1, 0, 1, 2, 2]
num_partitions: 3
x[0]:  tf.Tensor([1 4], shape=(2, ), dtype=int32)
x[1]:  tf.Tensor([3 5], shape=(2, ), dtype=int32)
x[2]:  tf.Tensor([2 6 7], shape=(3, ), dtype=int32)

```
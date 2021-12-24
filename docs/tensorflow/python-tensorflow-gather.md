# python–tensorlow . gather()

> 原文:[https://www.geeksforgeeks.org/python-tensorflow-gather/](https://www.geeksforgeeks.org/python-tensorflow-gather/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**聚集()**用于根据提供的索引对输入张量进行切片。

> **语法:**tensorflow . collect(参数、索引、validate _ indices、轴、batch_dims、名称)
> 
> **参数:**
> 
> *   **参数:**是秩大于等于轴+1 的张量。
> *   **指数:**它是 int32 或 int64 类型的张量。它的值应该在范围[0，params.shape[axis]内)。
> *   **轴:**是 int32 或 int64 类型的张量。它定义了应该从中收集索引的轴。默认值为 0，并且必须大于或等于 batch_dims。
> *   **batch_dims:** 表示批次维度数的整数。它必须小于或等于等级(指数)。
> *   **名称:**定义操作的名称。
> 
> **返回:**
> 
> 它返回一个与参数具有相同数据类型的张量。

**例 1:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input
data = tf.constant([1, 2, 3, 4, 5, 6])
indices = tf.constant([0, 1, 2, 1])

# Printing the input
print('data: ',data)
print('indices: ',indices)

# Calculating result
res = tf.gather(data, indices)

# Printing the result
print('res: ',res)
```

**输出:**

```
data:  tf.Tensor([1 2 3 4 5 6], shape=(6,), dtype=int32)
indices:  tf.Tensor([0 1 2 1], shape=(4,), dtype=int32)
res:  tf.Tensor([1 2 3 2], shape=(4,), dtype=int32)

```

**例 2:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input
data = tf.constant([[1, 2], [3, 4], [5, 6]])
indices = tf.constant([2, 0, 1])

# Printing the input
print('data: ',data)
print('indices: ',indices)

# Calculating result
res = tf.gather(data, indices)

# Printing the result
print('res: ',res)
```

**输出:**

```
data:  tf.Tensor(
[[1 2]
 [3 4]
 [5 6]], shape=(3, 2), dtype=int32)
indices:  tf.Tensor([2 0 1], shape=(3,), dtype=int32)
res:  tf.Tensor(
[[5 6]
 [1 2]
 [3 4]], shape=(3, 2), dtype=int32)

```
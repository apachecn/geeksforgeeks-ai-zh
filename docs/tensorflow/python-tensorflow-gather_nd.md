# Python–tensorflow . gather _ nd()

> 原文:[https://www.geeksforgeeks.org/python-tensorflow-gather_nd/](https://www.geeksforgeeks.org/python-tensorflow-gather_nd/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**聚集 _nd()** 用于根据提供的索引从输入张量聚集切片。

> **语法:** tensorflow.gather_nd(参数、索引、批处理参数、名称)
> 
> **参数:**
> 
> *   **参数**:秩大于等于轴+1 的张量。
> *   **指数:**它是 int32 或 int64 类型的张量。
> *   **batch_dims:** 表示批次维度数的整数。它必须小于等级(指数)。
> *   **名称:**定义操作的名称。
> 
> **返回:**
> 
> 它返回一个与参数具有相同数据类型的张量。

**例 1:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input
data = tf.constant([[1, 2], [3, 4], [5, 6]])
indices = tf.constant([[1], [0], [1]])

# Printing the input
print('data: ',data)
print('indices: ',indices)

# Calculating result
res = tf.gather_nd(data, indices)

# Printing the result
print('res: ',res)
```

**输出:**

```py
data:  tf.Tensor(
[[1 2]
 [3 4]
 [5 6]], shape=(3, 2), dtype=int32)
indices:  tf.Tensor(
[[1]
 [0]
 [1]], shape=(3, 1), dtype=int32)
res:  tf.Tensor(
[[3 4]
 [1 2]
 [3 4]], shape=(3, 2), dtype=int32)

```

**例 2:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input
data = tf.constant([[1, 2, 3], [3, 4, 5], [5, 6, 7]])
indices = tf.constant([[1, 0], [0, 2], [1, 2]])

# Printing the input
print('data: ',data)
print('indices: ',indices)

# Calculating result
res = tf.gather_nd(data, indices)

# Printing the result
print('res: ',res)
```

**输出:**

```py
data:  tf.Tensor(
[[1 2 3]
 [3 4 5]
 [5 6 7]], shape=(3, 3), dtype=int32)
indices:  tf.Tensor(
[[1 0]
 [0 2]
 [1 2]], shape=(3, 2), dtype=int32)
res:  tf.Tensor([3 3 5], shape=(3,), dtype=int32)

```
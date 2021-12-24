# Python – tensorflow.concat（）

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-conct/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**concat()** 用于沿一维连接张量。

> **语法:** tensorflow.concat(值、轴、名称)
> 
> **参数:**
> 
> *   **值:**是张量或张量列表。
> *   **轴:**表示要连接的维度的 0-D 张量。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**返回连接的张量。

**例 1:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input tensor
t1 = [[[1, 2], [3, 4]], [[5, 6], [7, 8]]]
t2 = [[[7, 4], [8, 4]], [[2, 10], [15, 11]]]

# Printing the input tensor
print('t1: ', t1)
print('t2: ', t2)

# Calculating result
res = tf.concat([t1, t2], 2)

# Printing the result
print('Result: ', res)
```

**输出:**

```
t1:  [[[1, 2], [3, 4]], [[5, 6], [7, 8]]]
t2:  [[[7, 4], [8, 4]], [[2, 10], [15, 11]]]
Result:  tf.Tensor(
[[[ 1  2  7  4]
  [ 3  4  8  4]]

 [[ 5  6  2 10]
  [ 7  8 15 11]]], shape=(2, 2, 4), dtype=int32)

```

**例 2:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input tensor
t1 = [[[1, 2], [3, 4]], [[5, 6], [7, 8]]]
t2 = [[[7, 4], [8, 4]], [[2, 10], [15, 11]]]

# Printing the input tensor
print('t1: ', t1)
print('t2: ', t2)

# Calculating result
res = tf.concat([t1, t2], 1)

# Printing the result
print('Result: ', res)
```

**输出:**

```
t1:  [[[1, 2], [3, 4]], [[5, 6], [7, 8]]]
t2:  [[[7, 4], [8, 4]], [[2, 10], [15, 11]]]
Result:  tf.Tensor(
[[[ 1  2]
  [ 3  4]
  [ 7  4]
  [ 8  4]]

 [[ 5  6]
  [ 7  8]
  [ 2 10]
  [15 11]]], shape=(2, 4, 2), dtype=int32)

```
# python–tensorlow . eye()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-eye/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**tensorflow.eye()** 用于生成单位矩阵。

> **语法:** tensorflow.eye( num_rows，num_columns，batch_shape，dtype，name)
> 
> **参数:**
> 
> *   **num_rows:** 是 int32 标量张量定义了结果矩阵中的行数。
> *   **num_columns(可选):**它是 int32 标量张量，定义结果矩阵中存在的列数。它的默认值是 num_rows。
> *   **batch_shape(可选):**它是 Python 整数的列表或元组，或者是一维 int32 张量。如果不是无，返回的张量将具有该形状的领先批量尺寸。
> *   **dtype(可选):**定义返回张量的 dtype。默认值为 float32。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**它返回一个形状的张量 batch _ shape+[num _ row，num_columns]。

**例 1:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input
num_rows = 5

# Printing the input
print('num_rows:', num_rows)

# Calculating result
res = tf.eye(num_rows)

# Printing the result
print('res: ', res)
```

**输出:**

```

num_rows: 5
res:  tf.Tensor(
[[1\. 0\. 0\. 0\. 0.]
 [0\. 1\. 0\. 0\. 0.]
 [0\. 0\. 1\. 0\. 0.]
 [0\. 0\. 0\. 1\. 0.]
 [0\. 0\. 0\. 0\. 1.]], shape=(5, 5), dtype=float32)

```

**例 2:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input
num_rows = 5
num_columns = 6
batch_shape = [3]

# Printing the input
print('num_rows:', num_rows)
print('num_columns:', num_columns)
print('batch_shape:', batch_shape)

# Calculating result
res = tf.eye(num_rows, num_columns, batch_shape)

# Printing the result
print('res: ', res)
```

**输出:**

```

num_rows: 5
num_columns: 6
batch_shape: [3]
res:  tf.Tensor(
[[[1\. 0\. 0\. 0\. 0\. 0.]
  [0\. 1\. 0\. 0\. 0\. 0.]
  [0\. 0\. 1\. 0\. 0\. 0.]
  [0\. 0\. 0\. 1\. 0\. 0.]
  [0\. 0\. 0\. 0\. 1\. 0.]]

 [[1\. 0\. 0\. 0\. 0\. 0.]
  [0\. 1\. 0\. 0\. 0\. 0.]
  [0\. 0\. 1\. 0\. 0\. 0.]
  [0\. 0\. 0\. 1\. 0\. 0.]
  [0\. 0\. 0\. 0\. 1\. 0.]]

 [[1\. 0\. 0\. 0\. 0\. 0.]
  [0\. 1\. 0\. 0\. 0\. 0.]
  [0\. 0\. 1\. 0\. 0\. 0.]
  [0\. 0\. 0\. 1\. 0\. 0.]
  [0\. 0\. 0\. 0\. 1\. 0.]]], shape=(3, 5, 6), dtype=float32)

```
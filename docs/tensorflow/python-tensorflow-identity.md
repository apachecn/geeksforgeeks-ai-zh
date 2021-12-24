# python–tensorlow . identity()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-identity/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**identity()** 返回一个与输入具有相同形状和内容的 Tensor。

> **语法:** tensorflow.identity(输入，名称)
> 
> **参数:**
> 
> *   **输入:**是张量。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**返回一个与输入形状和内容相同的张量。

**例 1:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input
data = tf.Variable([[1, 2, 3], [3, 4, 5], [5, 6, 7]])

# Printing the input
print('data: ', data)

# Calculating result
res = tf.identity(data)

# Printing the result
print('res: ', res)
```

**输出:**

```py

data:  <tf.Variable 'Variable:0' shape=(3, 3) dtype=int32, numpy=
array([[1, 2, 3],
       [3, 4, 5],
       [5, 6, 7]], dtype=int32)>
res:  tf.Tensor(
[[1 2 3]
 [3 4 5]
 [5 6 7]], shape=(3, 3), dtype=int32)

```

**例 2:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input
data = tf.constant([[1, 2, 3], [3, 4, 5], [5, 6, 7]])

# Printing the input
print('data: ', data)

# Calculating result
res = tf.identity(data)

# Printing the result
print('res: ', res)
```

**输出:**

```py

data:  tf.Tensor(
[[1 2 3]
 [3 4 5]
 [5 6 7]], shape=(3, 3), dtype=int32)
res:  tf.Tensor(
[[1 2 3]
 [3 4 5]
 [5 6 7]], shape=(3, 3), dtype=int32)

```
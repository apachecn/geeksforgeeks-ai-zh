# 张量流–如何从张量

创建数组

> 原文:[https://www . geesforgeks . org/tensorflow-how-create-a-numpy-ndarray-from-a-tensor/](https://www.geeksforgeeks.org/tensorflow-how-to-create-a-numpy-ndarray-from-a-tensor/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

为了从张量创建 numpy 数组，首先将张量转换为原张量。

> **使用的方法:**
> 
> *   **make_ndarray:** 此方法接受一个 TensorProto 作为输入，并返回一个 numpy 数组，其内容与 TensorProto 相同。

**例 1:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing Input
value = tf.constant([1, 15, 10], dtype = tf.float64)

# Printing the Input
print("Value: ", value)

# Converting Tensor to TensorProto
proto = tf.make_tensor_proto(value)

# Generating numpy array
res = tf.make_ndarray(proto)

# Printing the resulting numpy array
print("Result: ", res)
```

**输出:**

```py
Value:  tf.Tensor([ 1\. 15\. 10.], shape=(3, ), dtype=float64)
Result:  [ 1\. 15\. 10.]

```

**示例 2:** 本示例使用形状为(2，2)的张量，因此生成的数组的形状将为(2，2)。

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing Input
value = tf.constant([[1, 2], [3, 4]], dtype = tf.float64)

# Printing the Input
print("Value: ", value)

# Converting Tensor to TensorProto
proto = tf.make_tensor_proto(value)

# Generating numpy array
res = tf.make_ndarray(proto)

# Printing the resulting numpy array
print("Result: ", res)
```

**输出:**

```py
Value:  tf.Tensor(
[[1\. 2.]
 [3\. 4.]], shape=(2, 2), dtype=float64)
Result:  [[1\. 2.]
 [3\. 4.]]

```
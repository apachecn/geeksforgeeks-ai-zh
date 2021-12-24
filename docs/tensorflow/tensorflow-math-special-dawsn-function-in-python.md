# Python 中的 tensorflow.math.special.dawsn()函数

> 原文:[https://www . geesforgeks . org/tensorflow-math-special-dawsn-function-in-python/](https://www.geeksforgeeks.org/tensorflow-math-special-dawsn-function-in-python/)

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 python 库。

## dawsn()函数

**dawsn()** 用于计算 x 的元素式 Dawson 积分，定义为 exp(-x**2)乘以 0 到 x 的 exp(t**2)的积分，定义域为所有实数。

> **语法:**tensorflow . math . special . dawsn(x，name)
> 
> **参数:**
> 
> *   **x:** 是张量或稀疏张量。允许的数据类型是 float32 和 float64。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**返回与 x 相同数据类型的张量。

**例 1:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([ [-5, -7],[ 2, 0]], dtype=tf.float64)

# Printing the input tensor
print('a: ', a)

# Calculating result
res = tf.math.special.dawsn(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```
a:  tf.Tensor(
[[-5\. -7.]
 [ 2\.  0.]], shape=(2, 2), dtype=float64)
Result:  tf.Tensor(
[[-0.10213407 -0.07218097]
 [ 0.30134039  0\.        ]], shape=(2, 2), dtype=float64)
```

**例 2:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([1, 2, 3, 4, 5], dtype=tf.float64)

# Printing the input tensor
print('a: ', a)

# Calculating result
res = tf.math.special.dawsn(a)

# Printing the result
print('Result: ', res)
```

**输出:**

> 答:tf。张量([1。2.3.4.5.]，shape=(5，，，dtype=float64)
> 结果:tf。张量([0.53807951 0.30134039 0.17827103 0.129348 0.10213407]，形状=(5，，，dtype=float64)
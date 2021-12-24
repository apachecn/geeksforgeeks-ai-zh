# Python 中的 tensorflow.math.special.expint()函数

> 原文:[https://www . geesforgeks . org/tensorflow-math-special-expint-function-in-python/](https://www.geeksforgeeks.org/tensorflow-math-special-expint-function-in-python/)

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 Python 库。

## expint()函数

**expint()** 用于计算 x 的元素态指数积分，定义为 exp(t) / t 从-inf 到 x 的积分，定义域为所有正实数。

> **语法:**tensorflow . math . special . expint(x，name)
> 
> **参数:**
> 
> *   **x:** 是张量或稀疏张量。允许的数据类型是 float32 和 float64。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**返回与 x 相同数据类型的张量。

**例 1:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([ [-5, -7],[ 2, 0]], dtype=tf.float64)

# Printing the input tensor
print('a: ', a)

# Calculating result
res = tf.math.special.expint(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor(
[[-5\. -7.]
 [ 2\.  0.]], shape=(2, 2), dtype=float64)
Result:  tf.Tensor(
[[       nan        nan]
 [4.95423436       -inf]], shape=(2, 2), dtype=float64)
```

**例 2:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([1, 2, 3, 4, 5], dtype=tf.float64)

# Printing the input tensor
print('a: ', a)

# Calculating result
res = tf.math.special.expint(a)

# Printing the result
print('Result: ', res)
```

**输出:**

> 答:tf。张量([1。2.3.4.5.]，shape=(5，，，dtype=float64)
> 结果:tf。张量([1.89511782 4.95423436 9.93383257 19.63087447 40.18527536]，形状=(5，，，dtype=float64)
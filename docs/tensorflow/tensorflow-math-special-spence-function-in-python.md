# Python 中的 tensorflow.math.special.spence()函数

> 原文:[https://www . geesforgeks . org/tensorflow-math-special-Spence-function-in-python/](https://www.geeksforgeeks.org/tensorflow-math-special-spence-function-in-python/)

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 python 库。

## 菲涅耳斯宾塞()方法

**fresnel_spence()** 用于计算 x 的元素式 spence 积分，定义为 log(t)/(1–t)从 1 到 x 的积分，定义域为所有正实数。

> **语法:**tensorflow . math . special . Spence(x，name)
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
res = tf.math.special.spence(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor(
[[-5\. -7.]
 [ 2\.  0.]], shape=(2, 2), dtype=float64)
Result:  tf.Tensor(
[[        nan         nan]
 [-0.82246703  1.64493407]], shape=(2, 2), dtype=float64)
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
res = tf.math.special.spence(a)

# Printing the result
print('Result: ', res)
```

**输出:**

> 答:tf。张量([1。2.3.4.5.]，shape=(5，，，dtype=float64)
> 结果:tf。张量([ 0。-0.82246703-1.43674637-1.93937542-2.3699398]，形状=(5)，，dtype=float64)
# Python 中的 tensorflow.math.atan2()函数

> 原文:[https://www . geesforgeks . org/tensorflow-math-atan 2-python 中的函数/](https://www.geeksforgeeks.org/tensorflow-math-atan2-function-in-python/)

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 python 库。`**atan2()**`用于求 y/x 的元素方向反正切。

> **语法:** tf.math.atan2(y，x，name)
> 
> **参数:**
> 
> *   **y:** 是输入张量。这个张量允许的数据类型是 bfloat16，half，float32，float64。
> *   **y:** 是与 y 相同数据类型的输入张量。
> *   **名称(可选):**定义操作的名称。
>     
> 
> **返回:**返回与 x 相同数据类型的张量。

**例 1:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([ [-5, -7], [ 2, 0]], dtype = tf.float64)
b = tf.constant([ [1, 3], [9, 4]], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)
print('b: ', b)

# Calculating result
res = tf.math.atan2(a, b)

# Printing the result
print('Result: ', res)
```

**输出:**

```
a:  tf.Tensor(
[[-5\. -7.]
 [ 2\.  0.]], shape=(2, 2), dtype=float64)
b:  tf.Tensor(
[[1\. 3.]
 [9\. 4.]], shape=(2, 2), dtype=float64)
Result:  tf.Tensor(
[[-1.37340077 -1.16590454]
 [ 0.21866895  0\.        ]], shape=(2, 2), dtype=float64)

```

**例 2:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([ -.5, -.3, 0, .3, .5], dtype = tf.float64)
b = tf.constant([ 1, 2, 3, 4, 5], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)
print('b: ', b)

# Calculating tangent
res = tf.math.atan2(a, b)

# Printing the result
print('Result: ', res)
```

**输出:**

> 答:tf。张量([-0.5 -0.3 0。0.3±0.5]，shape=(5，，，dtype=float64)
> b: tf。张量([1。2.3.4.5.]，shape=(5，，，dtype=float64)
> 结果:tf。张量([-0.46364761 -0.14888995 0。0.07485985 0.09966865]，shape=(5，，，dtype=float64)
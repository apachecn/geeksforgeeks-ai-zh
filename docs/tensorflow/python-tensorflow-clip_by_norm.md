# Python–tensorflow . clip _ by _ norm()

> 原文:[https://www . geesforgeks . org/python-tensorflow-clip _ by _ norm/](https://www.geeksforgeeks.org/python-tensorflow-clip_by_norm/)

[TensorFlow](”https://www.geeksforgeeks.org/introduction-to-tensorflow/”) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 Python 库。

**clip_by_norm()** 用于将张量值裁剪到最大 L2 范数。

> **语法:** tensorflow.clip_by_norm(t，clip_norm，坐标轴，名称)
> 
> **参数:**
> 
> *   **t:** 需要裁剪的是输入张量。
> *   **clip_norm:** 定义最大裁剪值的是 0-D 标量张量。
> *   **轴(可选):**一维向量张量定义了用于计算 L2 范数的维度。如果没有提供，将使用所有尺寸。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**
> 
> 它返回一个张量。

**例 1:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input tensor
t = tf.constant([1, 2, 3, 4], dtype = tf.float64)
clip_norm = .8

# Printing the input tensor
print('t: ', t)
print('clip_norm: ', clip_norm)

# Calculating tangent
res = tf.clip_by_norm(t, clip_norm)

# Printing the result
print('Result: ', res)
```

**输出:**

```
t:  tf.Tensor([1\. 2\. 3\. 4.], shape=(4, ), dtype=float64)
clip_norm:  0.8
Result:  tf.Tensor([0.14605935 0.2921187  0.43817805 0.58423739], shape=(4, ), dtype=float64)

```

**例 2:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input tensor
t = tf.constant([1, 2, 3, 4], dtype = tf.float64)
clip_norm = 5.2

# Printing the input tensor
print('t: ', t)
print('clip_norm: ', clip_norm)

# Calculating tangent
res = tf.clip_by_norm(t, clip_norm)

# Printing the result
print('Result: ', res)
```

**输出:**

```
t:  tf.Tensor([1\. 2\. 3\. 4.], shape=(4, ), dtype=float64)
clip_norm:  5.2
Result:  tf.Tensor([0.94938577 1.89877153 2.8481573  3.79754307], shape=(4, ), dtype=float64)

```
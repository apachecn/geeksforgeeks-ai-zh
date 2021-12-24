# Python–tensorflow . clip _ by _ value()

> 原文:[https://www . geesforgeks . org/python-tensorflow-clip _ by _ value/](https://www.geeksforgeeks.org/python-tensorflow-clip_by_value/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**clip_by_value()** 用于将张量值裁剪到指定的最小值和最大值。

> **语法:** tensorflow.clip_by_value( t，clip_value_min，clip_value_max，名称)
> 
> **参数:**
> 
> *   **t:** 是输入 Tensor。
> *   **clip_value_min:** 定义最小剪辑值。
> *   **clip_value_max:** 定义最大剪辑值。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**
> 
> *它返回一个剪裁的张量。*

**例 1:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input tensor
t = tf.constant([1, 2, 3, 4], dtype = tf.float64)
clip_value_min = 2
clip_value_max = 5

# Printing the input tensor
print('t: ', t)
print('clip_min: ', clip_value_min)
print('clip_max: ', clip_value_max)

# Calculating result
res = tf.clip_by_vlaue(t, clip_min, clip_max)

# Printing the result
print('Result: ', res)
```

**输出:**

```
t:  tf.Tensor([1\. 2\. 3\. 4.], shape=(4, ), dtype=float64)
clip_min:  2
clip_max:  5
Result:  tf.Tensor([2\. 2\. 3\. 4.], shape=(4, ), dtype=float64)

```

**例 2:**

## 蟒蛇 3

```
# Importing the library
import tensorflow as tf

# Initializing the input tensor
t = tf.constant([[1, 2], [ 3, 4]], dtype = tf.float64)
clip_value_min = [2, 3]
clip_value_max = [5, 7]

# Printing the input tensor
print('t: ', t)
print('clip_min: ', clip_value_min)
print('clip_max: ', clip_value_max)

# Calculating result
res = tf.clip_by_value(t, clip_value_min, clip_value_max)

# Printing the result
print('Result: ', res)
```

**输出:**

```
t:  tf.Tensor(
[[1\. 2.]
 [3\. 4.]], shape=(2, 2), dtype=float64)
clip_min:  [2, 3]
clip_max:  [5, 7]
Result:  tf.Tensor(
[[2\. 3.]
 [3\. 4.]], shape=(2, 2), dtype=float64)

```
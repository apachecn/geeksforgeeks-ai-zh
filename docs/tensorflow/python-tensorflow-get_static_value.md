# Python–tensorflow . get _ static _ value()

> 原文:[https://www . geesforgeks . org/python-tensorflow-get _ static _ value/](https://www.geeksforgeeks.org/python-tensorflow-get_static_value/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**get_static_value()** 用于计算 Tensor 的静态值。如果无法计算静态值，它将返回无。

> **语法:** tensorflow.get_static_value(张量，部分)
> 
> **参数:**
> 
> *   **张量:**是需要计算静态值的输入张量。
> *   **部分:**真或假，默认值设置为假。它被设置为“真”以允许返回的数组具有部分计算值。
> 
> **返回:**返回一个包含计算结果的数组。

**例 1:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input
data = tf.constant([[1, 2, 3], [3, 4, 5], [5, 6, 7]])

# Printing the input
print('data: ',data)

# Calculating result
res = tf.get_static_value(data)

# Printing the result
print('res: ',res)
```

**输出:**

```py
data:  tf.Tensor(
[[1 2 3]
 [3 4 5]
 [5 6 7]], shape=(3, 3), dtype=int32)
res:  [[1 2 3]
 [3 4 5]
 [5 6 7]]
```

**例 2:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input
data = tf.Variable([[1, 2, 3], [3, 4, 5], [5, 6, 7]])

# Printing the input
print('data: ',data)

# Calculating result
res = tf.get_static_value(data)

# Printing the result
print('res: ',res)
```

**输出:**

```py
data:  <tf.Variable 'Variable:0' shape=(3, 3) dtype=int32, numpy=
array([[1, 2, 3],
       [3, 4, 5],
       [5, 6, 7]], dtype=int32)>
res:  None
```
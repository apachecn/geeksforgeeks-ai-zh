# Python–tensorflow . math . segment _ mean()

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-segment _ mean/](https://www.geeksforgeeks.org/python-tensorflow-math-segment_mean/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**segment_mean()** 用于求张量各段元素的平均值。

> **语法:**tensorflow . math . segment _ mean(数据，segment_ids，名称)
> 
> **参数:**
> 
> *   **数据:**是张量。允许的数据类型有 float32、float64、int32、uint8、int16、int8、int64、bfloat16、uint16、half、uint32、uint64。
> *   **segment_ids:** 是一维张量，取值排序。它的大小应该等于第一维数据的大小。允许的数据类型是 int32 和 int64。
> *   **名称(可选):**定义操作的名称。
> 
> **Return:** 它将数据类型的张量返回为 x。

**例 1:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
data = tf.constant([1, 2, 3])
segment_ids = tf.constant([2, 2, 2])

# Printing the input tensor
print('data: ', data)
print('segment_ids: ', segment_ids)

# Calculating result
res = tf.math.segment_mean(data, segment_ids)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
data:  tf.Tensor([1 2 3], shape=(3, ), dtype=int32)
segment_ids:  tf.Tensor([2 2 2], shape=(3, ), dtype=int32)
Result:  tf.Tensor([0 0 2], shape=(3, ), dtype=int32)

```

**例 2:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
data = tf.constant([[1, 2, 3], [4, 5, 6], [7, 8, 9]], dtype = float64)
segment_ids = tf.constant([0, 0, 2])

# Printing the input tensor
print('data: ', data)
print('segment_ids: ', segment_ids)

# Calculating result
res = tf.math.segment_mean(data, segment_ids)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
data:  tf.Tensor(
[[1\. 2\. 3.]
 [4\. 5\. 6.]
 [7\. 8\. 9.]], shape=(3, 3), dtype=float64)
segment_ids:  tf.Tensor([0 0 2], shape=(3, ), dtype=int32)
Result:  tf.Tensor(
[[2.5 3.5 4.5]
 [0\.  0\.  0\. ]
 [7\.  8\.  9\. ]], shape=(3, 3), dtype=float64)
```
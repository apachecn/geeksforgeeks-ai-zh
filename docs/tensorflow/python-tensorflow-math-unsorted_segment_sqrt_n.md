# Python–tensorflow . math . unsorted _ segment _ sqrt _ n()

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-unsorted _ segment _ sqrt _ n/](https://www.geeksforgeeks.org/python-tensorflow-math-unsorted_segment_sqrt_n/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**unsorted _ segment _ sqrt _ N()**用来求被 sqrt(N)除的线段的和。

> **语法:**tensorflow . math . unsorted _ segment _ sqrt _ n(数据，segment_ids，num_segments，名称)
> 
> **参数:**
> 
> *   **数据:**是张量。允许的数据类型是浮点型或复杂型。
> *   **segment_ids:** 是一维张量，取值排序。它的大小应该等于第一维数据的大小。它表示不同段标识的数量。允许的数据类型是 int32 和 int64。
> *   **num_segments:** 是张量。允许的数据类型是 int32 和 int64。
> *   **名称(可选):**定义操作的名称。
> 
> **Return:** 它将数据类型的张量返回为 x。

**例 1:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
data = tf.constant([1, 2, 3], dtype = tf.float64)
segment_ids = tf.constant([2, 2, 2])

# Printing the input tensor
print('data: ', data)
print('segment_ids: ', segment_ids)

# Calculating result
res = tf.math.unsorted_segment_sqrt_n(data, segment_ids, tf.constant(3))

# Printing the result
print('Result: ', res)
```

**输出:**

```py
data:  tf.Tensor([1\. 2\. 3.], shape=(3, ), dtype=float64)
segment_ids:  tf.Tensor([2 2 2], shape=(3, ), dtype=int32)
Result:  tf.Tensor([0\.         0\.         3.46410162], shape=(3, ), dtype=float64)

```

**例 2:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
data = tf.constant([[1, 2, 3], [4, 5, 6], [7, 8, 9]], dtype = tf.float64)
segment_ids = tf.constant([0, 0, 2])

# Printing the input tensor
print('data: ', data)
print('segment_ids: ', segment_ids)

# Calculating result
res = tf.math.unsorted_segment_sqrt_n(data, segment_ids, tf.constant(3))

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
[[3.53553391 4.94974747 6.36396103]
 [0\.         0\.         0\.        ]
 [7\.         8\.         9\.        ]], shape=(3, 3), dtype=float64)

```
# Python–tensorflow . math . top _ k()

> 原文:[https://www.geeksforgeeks.org/python-tensorflow-math-top_k/](https://www.geeksforgeeks.org/python-tensorflow-math-top_k/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**top_k()** 用于查找最后一个维度的前 k 个最大条目(沿着矩阵的每一行)。

> **语法:** tensorflow.math.top_k(输入，k，排序，名称)
> 
> **参数:**
> 
> *   **输入:**是 1 维以上的输入张量。
> *   **k(可选):**是 0-D 张量，默认值为 0。
> *   **已排序(可选):**如果设置为真，返回的元素将被排序。默认值为真。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**
> 
> *   **值:**沿每个最后维度切片的 k 个最大元素。
> *   **指数:**输入的最后一个维度内的数值指数。

**例 1:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([7, 2, 3, 9, 5], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)

# Calculating result
res = tf.math.top_k(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([7\. 2\. 3\. 9\. 5.], shape=(5, ), dtype=float64)
Result:  TopKV2(values=<tf.Tensor: shape=(1, ), dtype=float64, numpy=array([9.])>, 
    indices=<tf.Tensor: shape=(1, ), dtype=int32, numpy=array([3], dtype=int32)>)

```

**例 2:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([[7, 2, 3], [ 9, 5, 7]], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)

# Calculating result
res = tf.math.top_k(a, k = 2)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor(
[[7\. 2\. 3.]
 [9\. 5\. 7.]], shape=(2, 3), dtype=float64)
Result:  TopKV2(values=<tf.Tensor: shape=(2, 2), dtype=float64, numpy=
array([[7., 3.],
       [9., 7.]])>, indices=<tf.Tensor: shape=(2, 2), dtype=int32, numpy=
array([[0, 2],
       [0, 2]], dtype=int32)>)

```
# Python | tensorflow . math . Bessel _ i0()方法

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-Bessel _ i0-method/](https://www.geeksforgeeks.org/python-tensorflow-math-bessel_i0-method/)

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 python 库。

bessel_io()是 TensorFlow 数学模块中的方法。该方法用于计算张量的元素贝塞尔 i0。

```
Syntax:
tensorflow.math.bessel_i0(
    input, name
)

Argument:
1\. input: It's a tensor or SparseTensor for which element wise Bessel iO 
          need to be calculated. Allowed dtypes are half, float32, float64\. 
2\. name: It is an optional argument that defines the name for the operation.

Return:
A Tensor if Tensor is given as input otherwise SparseTensor having the same dtype as input.

```

**例 1:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# initializing constant tensor 
a = tf.constant([-1.5, 3 ], dtype=tf.float64)

# calculating bessel io
b = tf.math.bessel_i0(a)

# printing the input
print('Input: ',a)

# printing the output
print('Output: ',b)
```

**输出:**

```
Input:  tf.Tensor([-1.5  3\. ], shape=(2,), dtype=float64)
Output:  tf.Tensor([1.64672319 4.88079259], shape=(2,), dtype=float64)

```

**例 2:**

本示例使用 dtype 为 int32 的 tensor，这会引发错误。只允许使用 dtype half、float32、float64 的张量。

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# initializing constant tensor with dtype int32
a = tf.constant([1 , 3 ], dtype=tf.int32)

# printing the input
print('Input: ',a)

# calculating bessel io
b = tf.math.bessel_i0(a)
```

**输出:**

```
Input:  tf.Tensor([1 3], shape=(2,), dtype=int32)

NotFoundError                             Traceback (most recent call last)

<ipython-input-43-4c70ca866e4c> in <module>()
----> 1 b = tf.math.bessel_i0(a)

```
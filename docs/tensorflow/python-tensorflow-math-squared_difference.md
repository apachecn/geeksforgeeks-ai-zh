# Python–tensorflow . math . square _ difference()

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-squared _ difference/](https://www.geeksforgeeks.org/python-tensorflow-math-squared_difference/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**平方差()**用于计算元素方向(x-y)(x-y)。

> **语法:**tensorflow . math . square _ difference(x，y，name)
> 
> **参数:**
> 
> *   **x:** 是张量。允许的数据类型有 bfloat16、half、float32、float64、complex64、complex128。
> *   **y:** 它是一个与 x 相同数据类型的张量。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**返回张量。

**例 1:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([ -5, -7, 2, 5, 7], dtype = tf.float64)
b = tf.constant([ 1, 3, 9, 4, 7], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)
print('b: ', b)

# Calculating result
res = tf.math.squared_difference(a, b)

# Printing the result
print('Result: ', res)
```

**输出:**

```
a:  tf.Tensor([-5\. -7\.  2\.  5\.  7.], shape=(5, ), dtype=float64)
b:  tf.Tensor([1\. 3\. 9\. 4\. 7.], shape=(5, ), dtype=float64)
Result:  tf.Tensor([ 36\. 100\.  49\.   1\.   0.], shape=(5, ), dtype=float64)

```

**示例 2:** 进行复杂输入

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([ -5 + 3j, -7-2j, 2 + 1j, 5-7j, 7 + 3j], dtype = tf.complex128)
b = tf.constant([ 1 + 5j, 3 + 1j, 9-5j, 4 + 3j, 7-6j], dtype = tf.complex128)

# Printing the input tensor
print('a: ', a)
print('b: ', b)

# Calculating result
res = tf.math.squared_difference(a, b)

# Printing the result
print('Result: ', res)
```

**输出:**

```
a:  tf.Tensor([-5.+3.j -7.-2.j  2.+1.j  5.-7.j  7.+3.j], shape=(5, ), dtype=complex128)
b:  tf.Tensor([1.+5.j 3.+1.j 9.-5.j 4.+3.j 7.-6.j], shape=(5, ), dtype=complex128)
Result:  tf.Tensor([ 40.+0.j 109.+0.j  85.+0.j 101.+0.j  81.+0.j], shape=(5, ), dtype=complex128)

```
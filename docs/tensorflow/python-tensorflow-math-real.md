# Python–tensorflow . math . real()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-real/

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 python 库。 **real()** 用于寻找张量的元素态实部。

> **语法:** tf.math.real(x，name)
> 
> **参数:**
> 
> *   **x:** 是输入张量。这个张量允许的数据类型是 bfloat16，half，float32，float64，int32，int64，complex64，complex128。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**
> 它返回一个 float32 或 float64 类型的张量。。

**例 1:** 本例使用实张量。

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([1, 2, -3, -4], dtype = tf.float64)

# Printing the input tensor
print('Input: ', a)

# Calculating result
res = tf.math.real(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
Input:  tf.Tensor([ 1\.  2\. -3\. -4.], shape=(4, ), dtype=float64)
Result:  tf.Tensor([ 1\.  2\. -3\. -4.], shape=(4, ), dtype=float64)

```

**例 2:** 本例使用复张量。

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([1 + 3j, 2-5j, -3 + 7j, -4-8j], dtype = tf.complex128)

# Printing the input tensor
print('Input: ', a)

# Calculating result
res = tf.math.real( a)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
Input:  tf.Tensor([ 1.+3.j  2.-5.j -3.+7.j -4.-8.j], shape=(4, ), dtype=complex128)
Result:  tf.Tensor([ 1\.  2\. -3\. -4.], shape=(4, ), dtype=float64)
```
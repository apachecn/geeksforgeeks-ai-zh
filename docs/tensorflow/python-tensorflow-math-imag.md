# python–tensorlow . math . imag()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-imag/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**imag()** 用来求张量的虚部。

> **语法:** tensorflow.math.imag(输入，名称)
> 
> **参数:**
> 
> *   **输入:**是张量。允许的数据类型有 float、double、complex64 和 complex128。
> *   **名称(可选):**定义操作的名称
> 
> **返回:**它将数据类型的张量返回为 x。

**例 1:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([7, 8, 13, 11], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)

# Calculating the result
res = tf.math.imag(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([ 7\.  8\. 13\. 11.], shape=(4, ), dtype=float64)
Result:  tf.Tensor([0\. 0\. 0\. 0.], shape=(4, ), dtype=float64)

```

**例 2:**

## 蟒蛇 3

```py
# Importing the libraray
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([2 + 4j, 8 + 7j, 14 + 5j], dtype = tf.complex128)

# Printing the input tensor
print('a: ', a)

# Calculating the result
res = tf.math.imag(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([ 2.+4.j  8.+7.j 14.+5.j], shape=(3, ), dtype=complex128)
Result:  tf.Tensor([4\. 7\. 5.], shape=(3, ), dtype=float64)
```
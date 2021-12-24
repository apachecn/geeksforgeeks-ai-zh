# python–tensorlow . math . xload()

> 哎哎哎::1230【https://www . geeksforgeeks . org/python-tensorlow-math-xload/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**xlogy()** 用于计算元素方向的 x * log(y)。

> **语法:**tensorlow . math . xload G1 py(x，y，name)
> 
> **参数:**
> 
> *   **x:** 是张量。允许的数据类型有半，float32，float64，complex64，complex128。
> *   **y:** 它是一个与 x 相同数据类型的张量。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**返回张量。

**例 1:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([ -5, -7, 2, 0, 7], dtype = tf.float64)
b = tf.constant([ 1, 3, 9, 4, 7], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)
print('b: ', b)

# Calculating result
res = tf.math.xlogy(a, b)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([-5\. -7\.  2\.  0\.  7.], shape=(5, ), dtype=float64)
b:  tf.Tensor([1\. 3\. 9\. 4\. 7.], shape=(5, ), dtype=float64)
Result:  tf.Tensor([-0\.         -7.69028602  4.39444915  0\.         13.62137104], shape=(5, ), dtype=float64)

```

**例 2:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([ -5 + 2j, -7-5j, 2 + 2j, 5-3j, 7 + 6j], dtype = tf.complex128)
b = tf.constant([ 0 + 0j, 3-1j, 9 + 5j, 4-3j, -6-8j], dtype = tf.complex128)

# Printing the input tensor
print('a: ', a)
print('b: ', b)

# Calculating result
res = tf.math.xlogy(a, b)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([-5.+2.j -7.-5.j  2.+2.j  5.-3.j  7.+6.j], shape=(5, ), dtype=complex128)
b:  tf.Tensor([ 0.+0.j  3.-1.j  9.+5.j  4.-3.j -6.-8.j], shape=(5, ), dtype=complex128)
Result:  tf.Tensor(
[        inf       -infj -9.6678006 -3.50420885j  3.64924209+5.6776361j
  6.11668624-8.04581928j 29.40388026-1.68457149j], shape=(5, ), dtype=complex128)

```
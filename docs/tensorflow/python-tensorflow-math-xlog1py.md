# python–tensorlow . math . xload G1 py()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-xload 1g py/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**xlog1py()** 用于计算元素方向 x * log1p(y)。

> **语法:**tensorlow . math . xload G1 py(x，y，name)
> 
> **参数:**
> 
> *   **x:** 是张量。允许的数据类型有 bfloat16、half、float32、float64、complex64、complex128。
> *   **y:** 是张量。允许的数据类型有 bfloat16、half、float32、float64、complex64、complex128。
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
res = tf.math.xlog1py(a, b)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([-5\. -7\.  2\.  0\.  7.], shape=(5, ), dtype=float64)
b:  tf.Tensor([1\. 3\. 9\. 4\. 7.], shape=(5, ), dtype=float64)
Result:  tf.Tensor([-3.4657359  -9.70406053  4.60517019  0\.         14.55609079], shape=(5, ), dtype=float64)

```

**例 2:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf
import numpy as np

# Initializing the input tensor
a = tf.constant([ -5 + 2j, -7-5j, 2 + 2j, 5-3j, 7 + 6j], dtype = tf.complex128)
b = tf.constant([ 0 + 0j, 3-1j, 9 + 5j, 4-3j, -6-8j], dtype = tf.complex128)

# Printing the input tensor
print('a: ', a)
print('b: ', b)

# Calculating result
res = tf.math.xlog1py(a, b)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([-5.+2.j -7.-5.j  2.+2.j  5.-3.j  7.+6.j], shape=(5, ), dtype=complex128)
b:  tf.Tensor([ 0.+0.j  3.-1.j  9.+5.j  4.-3.j -6.-8.j], shape=(5, ), dtype=complex128)
Result:  tf.Tensor(
[ -0\.        +0.j         -11.14114002-5.36818272j
   3.90101852+5.75560896j   7.19464281-7.99163829j
  28.48660115-1.43986039j], shape=(5, ), dtype=complex128)

```
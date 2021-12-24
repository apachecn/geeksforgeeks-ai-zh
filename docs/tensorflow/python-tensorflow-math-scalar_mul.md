# python–tensorlow . math . scalar _ mul()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-scalar _ mul/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**scalar_mul()** 用于将张量与标量相乘。

> **语法:** tf.math.scalar_mul( scalar，x，name)
> 
> **参数:**
> 
> *   **标量:**是已知形状的 0-D 标量张量。
> *   **x:** 这是一个需要缩放的张量。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**
> 
> 它返回与 x 相同数据类型的张量。

**例 1:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the input tensor
scalar = (5)
a = tf.constant([2.5, 5.5, 1.5, 6.5], dtype = tf.float64)

# Printing the input tensor
print('scalar: ', scalar)
print('a: ', a)

# Calculating result
res = tf.math.scalar_mul(scalar, a)

# Printing the result
print('Result: ', res)
```

**输出:**

```
scalar:  5
a:  tf.Tensor([2.5 5.5 1.5 6.5], shape=(4, ), dtype=float64)
Result:  tf.Tensor([12.5 27.5  7.5 32.5], shape=(4, ), dtype=float64)

```

**例 2:** 本例使用复张量。

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the input tensor
scalar = (5)
a = tf.constant([2.5 + 3j, 5.5 + 1j, 1.5 + 7j, 6.5 + 8j], dtype = tf.complex128)

# Printing the input tensor
print('scalar: ', scalar)
print('a: ', a)

# Calculating result
res = tf.math.scalar_mul(scalar, a)

# Printing the result
print('Result: ', res)
```

**输出:**

```
scalar:  5
a:  tf.Tensor([2.5+3.j 5.5+1.j 1.5+7.j 6.5+8.j], shape=(4, ), dtype=complex128)
Result:  tf.Tensor([12.5+15.j 27.5 +5.j  7.5+35.j 32.5+40.j], shape=(4, ), dtype=complex128)

```
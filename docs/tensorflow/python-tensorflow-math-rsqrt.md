# python–tensorlow . math . rsqrt()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-rsqrt/

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 python 库。 **rsqrt()** 用于求 x 平方根的元素倒数。

> **语法:** tf.math.rsqrt(x，name)
> 
> **参数:**
> 
> *   **x:** 是输入张量。这个张量允许的数据类型是 bfloat16，half，float32，float64。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**
> 返回一个与 x 相同数据类型的张量

**例 1:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([.2, 1.6, 3.7, 1], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)

# Calculating result
res = tf.math.rsqrt(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([0.2 1.6 3.7 1\. ], shape=(4, ), dtype=float64)
Result:  tf.Tensor([2.23606798 0.79056942 0.51987524 1\.        ], shape=(4, ), dtype=float64)

```

**例 2:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([2.5, 5.5, 1.5, 6.5], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)

# Calculating result
res = tf.math.rsqrt(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([2.5 5.5 1.5 6.5], shape=(4, ), dtype=float64)
Result:  tf.Tensor([0.63245553 0.42640143 0.81649658 0.39223227], shape=(4, ), dtype=float64)

```
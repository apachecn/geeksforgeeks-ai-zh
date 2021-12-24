# Python–tensorflow . math . minimum()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-minimum/

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 python 库。**最小值()**用来求 x 和 y 的元素方向最大值，具体是返回 x < y？x : y。

> **语法:** tf.math.minimum(x，y，name)
> 
> **参数:**
> 
> *   **x:** 是输入张量。这个张量允许的数据类型是 bfloat16，half，float32，float64，int32，int64。
> *   **y:** 是与 x 相同数据类型的输入张量。
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
a = tf.constant([.2, .5, .7, 1], dtype = tf.float64)
b = tf.constant([.1, .3, 1, 5], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)
print('b: ', b)

# Calculating result
res = tf.math.minimum(x = a, y = b)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([0.2 0.5 0.7 1\. ], shape=(4, ), dtype=float64)
b:  tf.Tensor([0.1 0.3 1\.  5\. ], shape=(4, ), dtype=float64)
Result:  tf.Tensor([0.1 0.3 0.7 1\. ], shape=(4, ), dtype=float64)

```

**例 2:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([-2, -5, 7, 1], dtype = tf.int64)
b = tf.constant([-1, -6, 8, 0], dtype = tf.int64)

# Printing the input tensor
print('a: ', a)
print('b: ', b)

# Calculating result
res = tf.math.minimum(x = a, y = b)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([-2 -5  7  1], shape=(4, ), dtype=int64)
b:  tf.Tensor([-1 -6  8  0], shape=(4, ), dtype=int64)
Result:  tf.Tensor([-2 -6  7  0], shape=(4, ), dtype=int64)

```
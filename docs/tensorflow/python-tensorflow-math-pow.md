# Python–tensorflow . math . pow()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-pow/

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 python 库。 **pow()** 用来寻找元素智慧 x^y.

> **语法:** tf.math.pow(x，y，name)
> 
> **参数:**
> 
> *   **x:** 是输入张量。这个张量允许的数据类型是 float16、float32、float64、int32、int64、complex64 或 complex128。
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
res = tf.math.pow(x = a, y = b)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([0.2 0.5 0.7 1\. ], shape=(4, ), dtype=float64)
b:  tf.Tensor([0.1 0.3 1\.  5\. ], shape=(4, ), dtype=float64)
Result:  tf.Tensor([0.85133992 0.8122524  0.7        1\.        ], shape=(4, ), dtype=float64)

```

**示例 2:** 本示例使用 y 中的负值会产生错误。

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([2, 5, 7, 1], dtype = tf.int64)
b = tf.constant([-1, -6, 8, 0], dtype = tf.int64)

# Printing the input tensor
print('a: ', a)
print('b: ', b)

# Calculating result
res = tf.math.pow(x = a, y = b)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([2 5 7 1], shape=(4, ), dtype=int64)
b:  tf.Tensor([-1 -6  8  0], shape=(4, ), dtype=int64)

---------------------------------------------------------------------------

InvalidArgumentError                      Traceback (most recent call last)

 in ()
     11 
     12 # Calculating result
---> 13 res = tf.math.pow(x = a, y = b)
     14 
     15 # Printing the result

4 frames

/usr/local/lib/python3.6/dist-packages/six.py in raise_from(value, from_value)

InvalidArgumentError: Integers to negative integer powers are not allowed [Op:Pow]

```
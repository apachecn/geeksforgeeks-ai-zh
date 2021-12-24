# tensorlow–python 中的 linspace()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-linspace-in-python/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。在多次使用 TensorFlow 时，我们需要在一个时间间隔内生成均匀间隔的值。

> *   **tensorflow. linespace ():** This method takes the starting tensor, the ending tensor, the number of values and the axis, and returns a tensor with a specified number of equally spaced values.

**例 1:**

```py
# importing the library
import tensorflow as tf

# Initializing Input
start = tf.constant(1, dtype = tf.float64)
end = tf.constant(5, dtype = tf.float64)
num = 5

# Printing the Input
print("start: ", start)
print("end: ", end)
print("num: ", num)

# Getting evenly spaced values
res = tf.linspace(start, end, num)

# Printing the resulting tensor
print("Result: ", res)
```

**输出:**

```py
start:  tf.Tensor(1.0, shape=(), dtype=float64)
end:  tf.Tensor(5.0, shape=(), dtype=float64)
num:  5
Result:  tf.Tensor([1\. 2\. 3\. 4\. 5.], shape=(5, ), dtype=float64)

```

**示例 2:** 该示例使用二维张量，在提供不同的轴值时，将生成不同的张量。这种均匀间隔的值生成类型目前在夜间版本中是允许的。

```py
# importing the library
import tensorflow as tf

# Initializing Input
start = tf.constant((1, 15), dtype = tf.float64)
end = tf.constant((10, 35), dtype = tf.float64)
num = 5

# Printing the Input
print("start: ", start)
print("end: ", end)
print("num: ", num)

# Getting evenly spaced values
res = tf.linspace(start, end, num, axis = 0)

# Printing the resulting tensor
print("Result 1: ", res)

# Getting evenly spaced values
res = tf.linspace(start, end, num, axis = 1)

# Printing the resulting tensor
print("Result 2: ", res)
```

**输出:**

```py

start:  tf.Tensor([ 1\. 15.], shape=(2, ), dtype=float64)
end:  tf.Tensor([10\. 35.], shape=(2, ), dtype=float64)
num:  5
Result 1:  tf.Tensor(
[[ 1\.   15\.  ]
 [ 3.25 20\.  ]
 [ 5.5  25\.  ]
 [ 7.75 30\.  ]
 [10\.   35\.  ]], shape=(5, 2), dtype=float64)

Result 2:  tf.Tensor(
[[ 1\.    3.25  5.5   7.75 10\.  ]
 [15\.   20\.   25\.   30\.   35\.  ]], shape=(2, 5), dtype=float64)

```
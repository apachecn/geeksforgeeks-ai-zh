# Python–tensorflow . math . invert _ arrangement()

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-invert _ arrange/](https://www.geeksforgeeks.org/python-tensorflow-math-invert_permutation/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**invert _ 置换()**用于计算张量的逆置换。

> **语法:**tensorflow . math . invert _ arrangement(x，name)
> 
> **参数:**
> 
> *   **x:** 是一维张量。允许的数据类型是 int32 和 int64。张量值应该在[0，4]的范围内。
> *   **名称(可选):**定义操作的名称
> 
> **返回:**它将数据类型的张量返回为 x。

**例 1:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([1, 2, 3, 0], dtype = tf.int64)

# Printing the input tensor
print('a: ', a)

# Calculating the result
res = tf.math.invert_permutation(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([1 2 3 0], shape=(4, ), dtype=int64)
Result:  tf.Tensor([3 0 1 2], shape=(4, ), dtype=int64)
```

**示例 2:** 本示例使用超出范围的值。它将引发无效文档错误

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([1, 2, 3, 4], dtype = tf.int64)

# Printing the input tensor
print('a: ', a)

# Calculating the result
res = tf.math.invert_permutation(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([1 2 3 4], shape=(4, ), dtype=int64)

---------------------------------------------------------------------------

InvalidArgumentError                      Traceback (most recent call last)

 in ()
      9 
     10 # Calculating the result
---> 11 res = tf.math.invert_permutation(a)
     12 
     13 # Printing the result

2 frames

/usr/local/lib/python3.6/dist-packages/six.py in raise_from(value, from_value)

InvalidArgumentError: 4 is not between 0 and 4 [Op:InvertPermutation]
```
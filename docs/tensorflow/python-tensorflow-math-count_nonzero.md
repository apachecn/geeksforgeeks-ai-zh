# Python–tensorflow . math . count _ 非零()

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-count _ 非零/](https://www.geeksforgeeks.org/python-tensorflow-math-count_nonzero/)

[TensorFlow](https://www.geeksforgeeks.org/introduction-to-tensorflow/) 是谷歌为开发机器学习模型和深度学习神经网络而设计的开源 Python 库。

**count _ 非零()**用于计算张量中非零元素的数量。

> **语法:**TF . math . count _ 非零(输入，轴，keepdim，数据类型，名称)
> 
> **参数:**
> 
> *   **输入:**是一个需要缩小的张量。
> *   **轴(可选):**定义需要减少输入的轴。允许的范围是[-rank(输入)，rank(输入))。如果未给出任何值，则默认值为无，即输入将沿所有轴减少。
> *   **保持尺寸(可选):**如果为真，将保留长度为 1 的缩小尺寸。
> *   **数据类型(可选):**定义输出数据类型。如果 int32，则为默认值。
> *   **名称(可选):**定义操作的名称。
> 
> **返回:**
> 
> 它返回包含非零值数量的张量。

**例 1:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# initializing the input
a = tf.constant([1,0,2,5,0], dtype = tf.int32)  # 3 non-zero

# Printing the input
print("Input: ",a)

# Counting non-zero
res  = tf.math.count_nonzero(a)

# Printing the result
print("No of non-zero elements: ",res)
```

**输出:**

```
Input:  tf.Tensor([1 0 2 5 0], shape=(5,), dtype=int32)
No of non-zero elements:  tf.Tensor(3, shape=(), dtype=int64)
```

**例 2:** 当输入张量为类型字符串时，**“**被认为是空字符串。 **" "** 为非零。

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# initializing the input
a = tf.constant([""," ","a","b"])  # 3 non-zero

# Printing the input
print("Input: ",a)

# Counting non-zero
res  = tf.math.count_nonzero(a)

# Printing the result
print("No of non-zero elements: ",res)
```

**输出:**

```
Input:  tf.Tensor([b'' b' ' b'a' b'b'], shape=(4,), dtype=string)
No of non-zero elements:  tf.Tensor(3, shape=(), dtype=int64)
```
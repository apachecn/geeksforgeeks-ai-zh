# Python–tensorflow . math . less()

> 原文:[https://www.geeksforgeeks.org/python-tensorflow-math-less/](https://www.geeksforgeeks.org/python-tensorflow-math-less/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**less()** 用于寻找 x < y 的元素智慧真值，支持广播

> **语法:** tensorflow.math.less( x，y，name)
> 
> **参数:**
> 
> *   **x:** 它是张量。允许的数据类型有 float32、float64、int32、uint8、int16、int8、int64、bfloat16、uint16、half、uint32、uint64。
> *   **y:** 它是与 x 相同数据类型的张量。
> *   **名称(可选):**定义操作的名称
> 
> **返回:**返回 bool 类型的张量。

**例 1:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([7, 8, 13, 11], dtype = tf.float64)
b = tf.constant([2, 13, 14, 5],  dtype = tf.float64)

# Printing the input tensor
print('a: ', a)
print('b: ', b)

# Finding truth value
res = tf.math.less(x = a, y = b)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([ 7\.  8\. 13\. 11.], shape=(4, ), dtype=float64)
b:  tf.Tensor([ 2\. 13\. 14\.  5.], shape=(4, ), dtype=float64)
Result:  tf.Tensor([False  True  True False], shape=(4, ), dtype=bool)
```

**示例 2:** 在该示例中，将在输入时执行广播。

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([7, 8, 13, 11], dtype = tf.float64)
b = (9)

# Printing the input tensor
print('a: ', a)
print('b: ', b)

# Finding truth value
res = tf.math.less(x = a, y = b)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([ 7\.  8\. 13\. 11.], shape=(4, ), dtype=float64)
b:  9
Result:  tf.Tensor([ True  True False False], shape=(4, ), dtype=bool)
```
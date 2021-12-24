# Python–tensorflow . math . is _ non _ reducing()

> 原文:[https://www . geesforgeks . org/python-tensorflow-math-is _ non _ reducing/](https://www.geeksforgeeks.org/python-tensorflow-math-is_non_decreasing/)

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**是 _ non _ reducing()**如果 x 是非递减的，则返回 true。

> **语法:**tensorflow . math . is _ non _ reducing(x，name)
> 
> **参数:**
> 
> *   **x:** 是数值张量。
> *   **名称(可选):**定义操作的名称
> 
> **返回:**返回数据类型布尔的张量。

**例 1:**

## 蟒蛇 3

```py
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([2, 3, 3, 5], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)

# Calculating the result
res = tf.math.is_non_decreasing(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([2\. 3\. 3\. 5.], shape=(4, ), dtype=float64)
Result:  tf.Tensor(True, shape=(), dtype=bool)
```

**例 2:**

## 蟒蛇 3

```py
# Importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([7, 8, 13, 11], dtype = tf.float64)

# Printing the input tensor
print('a: ', a)

# Calculating the result
res = tf.math.is_non_decreasing(a)

# Printing the result
print('Result: ', res)
```

**输出:**

```py
a:  tf.Tensor([ 7\.  8\. 13\. 11.], shape=(4, ), dtype=float64)
Result:  tf.Tensor(False, shape=(), dtype=bool)
```
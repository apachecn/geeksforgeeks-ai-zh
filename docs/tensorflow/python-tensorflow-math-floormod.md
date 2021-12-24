# python–tensorlow . math . flood mode()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math flood mode/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**floormod()** 用于计算 x 除以 y 的元素方式余数。

> **语法:**tensorlow . math . flood mode(x，y，name)
> 
> **参数:**
> 
> *   **x:** 它是张量。允许的数据类型有 int32、int64、bfloat16、half、float32、float64。
> *   **y:** 它是与 x 相同数据类型的张量。
> *   **名称(可选):**定义操作的名称
> 
> **返回:**返回张量。

**例 1:**

## 蟒蛇 3

```
# importing the library
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([7, 8, 13, 11], dtype = tf.float64)
b = tf.constant([2, 3, 4, 5],  dtype = tf.float64)

# Printing the input tensor
print('a: ', a)
print('b: ', b)

# Using floormod
res = tf.math.floormod(x = a, y = b)

# Printing the result
print('Result: ', res)
```

**输出:**

```
a:  tf.Tensor([ 7\.  8\. 13\. 11.], shape=(4, ), dtype=float64)
b:  tf.Tensor([2\. 3\. 4\. 5.], shape=(4, ), dtype=float64)
Result:  tf.Tensor([1\. 2\. 1\. 1.], shape=(4, ), dtype=float64)

```

**示例 2:** 在本示例中，第二张量中的一个值取为 0。

## 蟒蛇 3

```
# Importing the libraray
import tensorflow as tf

# Initializing the input tensor
a = tf.constant([7, 8, 13, 11], dtype = tf.float64)
b = tf.constant([2, 3, 4, 0],  dtype = tf.float64)

# Printing the input tensor
print('a: ', a)
print('b: ', b)

# Calculating result
res = tf.math.floormod(x = a, y = b)

# Printing the result
print('Result: ', res)
```

**输出:**

```
a:  tf.Tensor([ 7\.  8\. 13\. 11.], shape=(4, ), dtype=float64)
b:  tf.Tensor([2\. 3\. 4\. 0.], shape=(4, ), dtype=float64)
Result:  tf.Tensor([ 1\.  2\.  1\. nan], shape=(4, ), dtype=float64)
```
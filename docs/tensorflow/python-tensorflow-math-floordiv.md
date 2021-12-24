# python–tensorlow . math . flood rdiv()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-tensorlow-math-floodrdiv/

TensorFlow 是谷歌设计的开源 Python 库，用于开发机器学习模型和深度学习神经网络。

**floordiv()** 用于计算 x 除以 y 的元素方式除法，并将结果舍入到最负整数。

> **语法:**tensorlow . math . flood rdiv(x，y，name)
> 
> **参数:**
> 
> *   **x:** 它是一个具有实数值的张量。
> *   **y:** 它是一个具有实数值的张量。
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

# Calculating style division
res = tf.math.floordiv(x = a, y = b)

# Printing the result
print('Result: ', res)
```

**输出:**

```
a:  tf.Tensor([ 7\.  8\. 13\. 11.], shape=(4, ), dtype=float64)
b:  tf.Tensor([2\. 3\. 4\. 5.], shape=(4, ), dtype=float64)
Result:  tf.Tensor([3\. 2\. 3\. 2.], shape=(4, ), dtype=float64)

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

# Calculating style division
res = tf.math.floordiv(x = a, y = b)

# Printing the result
print('Result: ', res)
```

**输出:**

```
a:  tf.Tensor([ 7\.  8\. 13\. 11.], shape=(4, ), dtype=float64)
b:  tf.Tensor([2\. 3\. 4\. 0.], shape=(4, ), dtype=float64)
Result:  tf.Tensor([ 3\.  2\.  3\. inf], shape=(4, ), dtype=float64)
```